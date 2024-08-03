npm install -g live-server
live-server

理解 HTML 文件在 live-server 中如何运行 React 的过程，可以通过以下步骤进行解释：

浏览器请求 HTML 文件：

浏览器通过 live-server 请求 index.html 文件。
浏览器加载 HTML 文件：

浏览器接收到 index.html 文件并解析 HTML 结构。
浏览器加载 React 和 Babel：

浏览器按照 HTML 文件中的 <script> 标签依次加载 React、ReactDOM 和 Babel 的脚本。
这些脚本被加载后，会在浏览器中提供 React 和 Babel 的功能。
编译和执行 JSX：

浏览器遇到 <script type="text/babel"> 标签时，Babel 会将其中的 JSX 代码实时编译为普通的 JavaScript 代码。
编译后的 JavaScript 代码被执行，调用 ReactDOM.render 方法，将 React 组件渲染到指定的 DOM 节点中。
下面是这个过程的图示：

javascript
复制代码
+---------------------------+
| 1. 浏览器请求 HTML 文件 |
| ----------------------> |
| |
| |
| live-server |
+---------------------------+
|
v
+---------------------------+
| 2. 浏览器加载 HTML 文件 |
| |
| <html> |
| <head> |
| <script src="react.js"></script> <--- 3. 加载 React 和 Babel
| <script src="react-dom.js"></script>|
| <script src="babel.js"></script> |
| </head> |
| <body> |
| <div id="app"></div> |
| <script type="text/babel"> |
| ReactDOM.render(<h1>Hello world</h1>, document.querySelector("#app")); |
| </script> |
| </body> |
| </html> |
+---------------------------+
|
v
+---------------------------+
| 3. 浏览器加载 React 和 Babel 脚本 |
| |
| - React 和 ReactDOM 脚本被加载 |
| - Babel 脚本被加载 |
+---------------------------+
|
v
+---------------------------+
| 4. 编译和执行 JSX |
| |
| - Babel 编译 JSX 为 JavaScript |
| - ReactDOM.render 被调用 |
| - React 组件被渲染到 #app 节点 |
+---------------------------+
通过这个图示，你可以看到 live-server 只是简单地提供静态文件，而浏览器负责加载、解析和执行 HTML 和 JavaScript 代码。React 和 Babel 的功能通过加载 CDN 脚本在浏览器中实现，最终实现 React 组件的渲染。

npm init -y
npm install react react-dom react-scripts --save-dev
"scripts": {
"start": "react-scripts start"
},
npm start

![](https://www.fullstackreact.com/assets/images/30days/30-days-of-react-header.jpg)

<hr />
<h1 align="center">
  30 Days of React
</h1>
<p align="center">
<img src="./images/readme/30-days-of-react-book-cover-2-as-book-220.png"/>
</p>
<h2 align="center">
  ✨ An Introduction to React - <b>in 30 Bite-Size Morsels</b> ✨
</h2>
<p align="center">
Written by <a href="https://fullstack.io">Fullstack.io</a> and <a href="#contributors">friends</a>
</p>
<p align="center">
<a href="https://app.monstercampaigns.com/c/opsh28ygz42xhvtlq4vd/">
<img src="./images/readme/download-the-pdf-button.png" width="484" height="83" />
</a>
</p>
<hr />

# 🚀 Introduction

Over the next 30 days, we'll walk through everything you need to know to work with React. From the very beginning through testing and deployment of our first app.

This repository contains the entire source and content for the article series of [30 Days of React](https://www.fullstackreact.com/30-days-of-react) hosted by the [Fullstack React](https://www.fullstackreact.com/) team.

## 👀 What's inside?

<!-- prettier-ignore -->
| <a href='./day-01'><img src='./day-01/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-01'>What is React?</a><h4> | <a href='./day-02'><img src='./day-02/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-02'>What is JSX?</a><h4> | <a href='./day-03'><img src='./day-03/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-03'>Our First Components</a><h4> | <a href='./day-04'><img src='./day-04/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-04'>Complex Components</a><h4> | <a href='./day-05'><img src='./day-05/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-05'>Data-Driven</a><h4> |
| :---: | :---: | :---: | :---: | :---: |
| <a href='./day-06'><img src='./day-06/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-06'>State</a><h4> | <a href='./day-07'><img src='./day-07/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-07'>Lifecycle Hooks</a><h4> | <a href='./day-08'><img src='./day-08/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-08'>Packaging and PropTypes</a><h4> | <a href='./day-09'><img src='./day-09/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-09'>Styles</a><h4> | <a href='./day-10'><img src='./day-10/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-10'>Interactivity</a><h4> |
| <a href='./day-11'><img src='./day-11/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-11'>Pure Components</a><h4> | <a href='./day-12'><img src='./day-12/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-12'>create-react-app</a><h4> | <a href='./day-13'><img src='./day-13/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-13'>Repeating Elements</a><h4> | <a href='./day-14'><img src='./day-14/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-14'>Fetching Remote Data</a><h4> | <a href='./day-15'><img src='./day-15/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-15'>Introduction to Promises</a><h4> |
| <a href='./day-16'><img src='./day-16/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-16'>Displaying Remote Data</a><h4> | <a href='./day-17'><img src='./day-17/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-17'>Client-side Routing</a><h4> | <a href='./day-18'><img src='./day-18/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-18'>Introduction to Flux</a><h4> | <a href='./day-19'><img src='./day-19/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-19'>Data Management with Redux</a><h4> | <a href='./day-20'><img src='./day-20/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-20'>Redux actions</a><h4> |
| <a href='./day-21'><img src='./day-21/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-21'>Redux Middleware</a><h4> | <a href='./day-22'><img src='./day-22/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-22'>Introduction to Testing</a><h4> | <a href='./day-23'><img src='./day-23/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-23'>Implementing Tests</a><h4> | <a href='./day-24'><img src='./day-24/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-24'>Testing the App</a><h4> | <a href='./day-25'><img src='./day-25/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-25'>Better Testing with Enzyme</a><h4> |
| <a href='./day-26'><img src='./day-26/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-26'>Integration Testing</a><h4> | <a href='./day-27'><img src='./day-27/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-27'>Deployment Introduction</a><h4> | <a href='./day-28'><img src='./day-28/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-28'>Deployment</a><h4> | <a href='./day-29'><img src='./day-29/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-29'>Continuous Integration</a><h4> | <a href='./day-30'><img src='./day-30/cover.jpg' width='140px;' /></a><h4 align='center'><a href='./day-30'>Wrap-up and More Resources</a><h4> |

## 👩‍🏫 How to use this repository

Each day contains a full React application, following the same procedure used to create the article series. Most days can be run using the same basic steps (and for the days that require a bit more work, check out the tutorial series on the blog).

The steps run any _30 Days of React_ project are:

We can run these steps using the following commands:

```bash
# install the dependencies
yarn install

# start the project
yarn start
```

Since all of the days are built using the fantastic [create-react-app](https://github.com/facebookincubator/create-react-app) tool, all of the commands are available from that project in every day.

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| <a href='http://willcodeforfoo.com'><img src='https://avatars1.githubusercontent.com/u/529?v=4' width='140px;'/><h4 align='center'><a href='http://willcodeforfoo.com'>Ari</a></h4> | <a href='https://newline.co'><img src='https://avatars2.githubusercontent.com/u/4318?v=4' width='140px;'/><h4 align='center'><a href='https://newline.co'>Nate Murray</a></h4> | <a href='https://codepen.io/PeterHYChan/'><img src='https://avatars3.githubusercontent.com/u/32804449?v=4' width='140px;'/><h4 align='center'><a href='https://codepen.io/PeterHYChan/'>Peter Ho Yeung Chan</a></h4> | <a href='https://github.com/harms280'><img src='https://avatars2.githubusercontent.com/u/10542951?v=4' width='140px;'/><h4 align='center'><a href='https://github.com/harms280'>Aaron</a></h4> |
| :---: | :---: | :---: | :---: |

<!-- ALL-CONTRIBUTORS-LIST:END -->

---

# Fullstack React Book

<a href="https://fullstackreact.com">
<img align="right" src="images/readme/fullstack-react-hero-book.png" alt="Fullstack React Book" width="155" height="250" />
</a>

This repo was written and is maintained by the [Fullstack React](https://fullstackreact.com) team. In the book we cover many more projects like this. We walk through each line of code, explain why it's there and how it works.

_30 Days of React_ covers only the early basics of React. If you're looking to learn how to build real-world React apps, including libraries from the React ecosystem, there's no faster way than by spending a few hours with the Fullstack React book.

<div style="clear:both"></div>
