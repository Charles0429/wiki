---
title: mac开发环境配置
date: 2017-07-02 22:56:37
category: tools
tags:
  - mac

---

# 简介

本文主要介绍了macos上一些常见的设置和效率工具的安装

# 常用设置

## 键盘设置

键盘的设置主要有：

1. 重复按键时提升速度，在vim中移动光标的时候就不会卡顿了
2. 将F1-F12设置成标准的功能键

![](http://o8m1nd933.bkt.clouddn.com/wiki/keyboard.png)

如果是用普通的外接键盘的话，上面的windows键是和mac下的command键对应的，但是，普通键盘的option键和command键的顺序和mac原生键盘的键位是反的，所以还需要设置一下：

打开系统偏好设置->键盘->修饰键

![](http://o8m1nd933.bkt.clouddn.com/wiki/outer_keyboard.png)

还需要设置一下输入法的切换快捷键：

系统偏好设置->键盘->快捷键->输入源

![](http://o8m1nd933.bkt.clouddn.com/wiki/input_method.png)

## 快速屏保设置

对于上班的同学，经常吃饭的时候需要锁屏，mac下比较快速的锁屏设置方式如下：

打开系统偏好设置->桌面与屏幕保护程序->屏幕保护程序->触发角

![](http://o8m1nd933.bkt.clouddn.com/wiki/sleep.png)

为了绝对的安全，还可以设置成进入屏幕保护程序后，需要马上用密码才能进入系统的方式，具体的是：

系统偏好设置->安全性与隐私性->通用

![](http://o8m1nd933.bkt.clouddn.com/wiki/password.png)

## 双屏幕Docker停留位置

一般用双屏幕时，会吧Docker栏停在大屏幕上，方便操作，设置如下:

系统偏好设置->显示器->排列，把上面的白色矩形条拖到大屏幕上即可


# 常用效率软件

## Manico

macos下的`Command+tab`组合键切换应用程序时只能按顺序一个个的切换，非常的不方面，而Mannico提供的是用快捷键的方式自动的切换应用，如下：

![](http://o8m1nd933.bkt.clouddn.com/wiki/launcher.png)

## Alfred

支持比macos下spotlight更强大的搜索功能，[传送门](http://macshuo.com/?p=625)

默认情况下Alfred是开启搜索文件的，可以在Prefrence里面设置开启

![](http://o8m1nd933.bkt.clouddn.com/wiki/alfred.png)

## Popclip

选中文字后会直接弹出`拷贝、粘贴`等浮动窗

![](http://o8m1nd933.bkt.clouddn.com/wiki/popclip.png)

对于某些程序，可能希望设置成Popclip禁用的状态，如下：

![](http://o8m1nd933.bkt.clouddn.com/wiki/popclip2.png)

## xtrafinder

xtrafinder支持像chrome一样的标签页，非常的方便，[传送门](https://www.trankynam.com/xtrafinder/)

效果图如下:

![](http://o8m1nd933.bkt.clouddn.com/wiki/xtrafinder.png)

## macdown

macos下的markdown软件，[传送门](http://macdown.uranusjr.com/)

## caffeine

防止mac休眠的软件，[传送门](https://itunes.apple.com/app/caffeine/id411246225)

## Moom
可以很方便调整应用窗口大小的软件，[传送门](https://itunes.apple.com/us/app/moom/id419330170?mt=12)

# 开发效率工具

## xcode

有的开发软件需要先安装xcode，这个可以在APP Store里面安装

## Homebrew

安装只需要一条命令
```
ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
```
安装好以后就可以用brew命令安装各种软件包了

## ZSH

zsh比默认的shell交互性更好，一般macos下已经自带了，可以直接切换即可

```
chsh -s /bin/zsh
```

## OH-MY-ZSH
主要是为了让终端变得更炫酷的，而且还有很多主题可以选择

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## iterm2

有关iterm2配置可以参照[传送门](http://laoshuterry.gitbooks.io/mac_os_setup_guide/content/4_ZshConfig.html)

## tmux
可以很方便的切换屏幕，以及保存在服务器上的工作状态，[传送门](http://mingxinglai.com/cn/2012/09/tmux/)

## dash
可以很方便的查阅文档

## macvim
macvim比原生的vim对macos系统更友好，
[安装](http://uzumaki-kyuubi-geeklife.com/2014/10/mac%E9%85%8D%E7%BD%AE%E5%AE%89%E8%A3%85macvim/)
[插件](http://ibpf.github.io/blog/2015/04/17/mac-vim-xiu-lian-ji-vundle/)
