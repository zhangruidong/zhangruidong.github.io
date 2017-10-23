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

