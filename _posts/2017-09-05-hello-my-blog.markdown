---
layout:     post
title:      "Hello my blog"
subtitle:   " \"Hello World, Hello Blog\""
date:       2017-09-05 12:00:00
author:     "Zrd"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 生活
---

> “Yeah It's on. ”


## 前言

Zrd 的 Blog 在折腾了三天后终于开通了。

作为一个前端程序员，博客要是挂在简书、知乎上太没有意思了，没什么自由度，界面也不好看，功能有限，不如自己折腾一下，做一个个人博客。


<p id = "build"></p>
---

## 如何实现

之前逛论坛的时候经常看到别人搭建的一些个人博客，就去了解了他们是如何实现的。结合自己的技术水平，发现jekyll + githubPage 是非常适合我的。实现起来快速、轻松。

其优点非常明显：

* **Markdown** 带来的优雅写作体验
* 非常熟悉的 Git workflow ，**Git Commit 即 Blog Post**
* 利用 GitHub Pages 的域名和免费无限空间，不用自己折腾主机
	* 如果需要自定义域名，也只需要简单改改 DNS 加个 CNAME 就好了 
* Jekyll 的自定制非常容易，基本就是个模版引擎

对于我来说就是在本地部署好jekyll，jekyll的原理很简单。
* Windows下可以直接装集成好的[Ruby installer](https://rubygems.org/pages/download)来进行安装
* 安装RubyGems，gem是一个ruby的包管理系统，可以用gem很方便的在本地安装ruby应用。
* 有了gem之后安装jekyll就很容易了，以前用过node和npm包安装，安装jekyll，直接在Terminal里面输入以下代码：
```$xslt
    $ gem install jekyll 
```
* 有了jelyll的环境，然后去folk了一个主题，感谢[hux](https://github.com/huxpro)
* 对主题上的功能和样式进行一些修改
* push到github上，我的blog就诞生了

## 后记
搭建博客是为了记录自己的学习和生活，这是见证自己成长过程的地方。

接下来需要做的事情就是：post！post！post！


