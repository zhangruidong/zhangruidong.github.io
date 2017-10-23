---
layout:     post
title:      "热模块"
subtitle:   "Webpack Hot Module Replacement Plugin"
date:       2017-09-06 12:00:00
author:     "Zrd"
header-img: "img/in-post/computer/computer-3.jepg"
catalog: true
tags:
    - 前端开发
    - webpack
---

## 前言
> 热模块替换，全称是Hot Module ReplaceMent(HMR)，理解成热模块替换或者模块热替换都可以，这个功能主要是用于开发过程中，对生产环境没有任何帮助。

热模块能给我们的开发带来很多便利，节省很多时间。

## 使用方法

1. 准备好环境，如node，webpack……

2. 新建一个项目，对package.json和webpack.config.js 做如下配置
```json
// package.json
{
  "name": "003",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack-dev-server --env development",
    "dev": "webpack-dev-server --env development",
    "build": "webpack --env production"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "html-webpack-plugin": "^2.28.0",
    "webpack": "^2.3.2",
    "webpack-dev-server": "^2.4.2"
  }
}

```

```js
// webpack.config.js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  devServer: {
    host: process.env.HOST, // Defaults to `localhost`
    port: 8080 // Defaults to 8080
  },
  entry: {
    app: "./app/app.js",
  },
  output: {
    path: path.resolve(__dirname,"build"),
    filename: '[name].js',
  },
  plugins: [
    new HtmlWebpackPlugin({
      title: 'hot replace',
    })
  ]
};
```

3. npm i

4. npm run dev 或者 npm run start 这些可以在package.json中的scripts中进行配置

5. 浏览器打开 localhost:8080 端口号可以在webpack.config.js中修改。


**热模块打包的资源是放在内存中的**




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


