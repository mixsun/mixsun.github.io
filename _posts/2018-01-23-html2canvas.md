---
layout: post
title: HTML内容转Canvas生成图片利器之html2canvas
date: 2018-01-23 16:01:52
---

![题图](/images/article/20180124.jpg)

html2canvas能够实现用户浏览器端的任何一部分进行截屏，渲染成一个canvas图片，不需要来自服务器端的任何渲染，整个生成过程都是由客户端浏览器创建。如果浏览器不支持canvas时，可以用flashcanvas或者exploreCanvas技术代替。
浏览器要求，支持（**ES6 Promise**）
Firefox 3.5+
Google Chrome
Opera 12+
IE9+
Safari 6+
![题图](/images/article/20180124-1.png)

基本语法

    <!-- html结构 -->
    <div id="capture" style="padding: 10px; background: #f5da55">
		<h4 style="color: #000; ">Hello world!</h4>
	</div>
	var options = {
		width:800,
		height:600
	};
    html2canvas(document.querySelector("#capture"),options).then(canvas => {
		document.body.appendChild(canvas)
	});

options参数可配置如：[参数url地址](http://html2canvas.hertzen.com/configuration)

[html2canvas官方地址](http://html2canvas.hertzen.com/)
[html2canvas github地址](https://github.com/niklasvh/html2canvas/)