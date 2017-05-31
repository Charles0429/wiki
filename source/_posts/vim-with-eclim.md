---
title: vim+eclim安装配置指南
date: 2017-05-31 20:00:37
category: tools
tags:
  - vim
---

# 介绍

本文介绍了vim+eclim的安装配置，主要是为了解决vim不方便查看函数调用栈的问题。

# 安装流程

## 安装jdk 1.8

由于我的系统已经安装好了，就不详述此部分的步骤了

## 下载eclipse

虽然官方的安装文档中推荐的是eclim2.6 + eclipse 4.6的配置，在这个配置下一直没有安装成功。因此，本文采用的是eclim2.5 + eclipse 4.5的版本。

首先，下载 eclipse for C/C++ IDE，下载链接为[eclipse Mars](https://eclipse.org/downloads/packages/release/Mars/2)

然后，解压

```
 tar -xvf eclipse-cpp-mars-2-linux-gtk-x86_64.tar.gz
```

## 下载eclim

下载eclim2.5版本，下载链接为[eclim2.5](https://sourceforge.net/projects/eclim/files/eclim/2.5.0/)

## 安装eclim

使用如下命令

```
java \
  -Dvim.files=$HOME/.vim \
  -Declipse.home=$HOME/eclipse \
  -jar eclim_2.5.0.jar install
```

这里假设eclipse是放在用户的home目录下的

## 启动eclim

```
eclipse/eclimd -b
```

## 检查是否安装成功

打开vim，执行`:PingEclim`，如果能正确显示eclim和eclipse的版本号，那么说明安装成功。

## 查看调用栈的例子

以leveldb源码为例，查看其某个函数的调用栈。

假设leveldb源码下载到$HOME/code/leveldb

首先，以leveldb目录建立project

```
ProjectCreate $HOME/code/levedb -n c++
```

接着，打开`table/block.cc`文件，查看`DecodeEntry`函数的调用栈，把光标移动到DecodeEntry上，然后执行如下命令

```
:CCallHierarchy
```

效果如下图：

![call graph](http://img.oserror.com/wiki/leveldb_call_graph.png)
