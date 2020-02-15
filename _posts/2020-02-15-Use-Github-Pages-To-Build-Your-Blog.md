---
layout: blog
title: Use Github Page To Build Your Blog
---
Github 提供了一种建立自己博客或者介绍自己项目网站的一种方式 -- Github Pages.

Github Pages 是基于 Jekyll 的， Jekyll 是一个把文字转换成静态网站或博客的系统。我们把博客按照 Jekyll 约定的格式提交到 Github， 在 Github 上打开 Github　Pages 功能，Github Pages 会用 Jekyll 把仓库中的内容打包并发布成静态网站。具体如何操作实现，[Jekyll][https://jekyllrb.com/docs/] 官网有详细的介绍，这篇文章是自己学习和总结的过程。

#### 第一步 安装 Jekyll
当然这一步对于已经熟练知道 Jekyll 的运行方式的同学是不必要的。但是对于新手，Jekyll里面的众多约定最好都亲自实现一下，在提交到 Github 之前在本地跑起来看一下效果还是很必要的。下面是在 Windows 系统下的安装流程。
1. Jekyll 是基于 Ruby 的，所以首先要安装 [Ruby（Ruby+Devkit 的版本）][https://rubyinstaller.org/downloads/]。
2. 使用如下命令安装 gems。
```shell
ridk install
```
3. 使用下面的命令安装 Jekyll。
```
gem install jekyll bundler
```
4. 最后跑一下下面这个命令，能显示 Jekyll 的版本就安装完成了。
```
jekyll -v
```

#### 第二步 写一个简单的网站跑起来
1. 首先我们建一个目录作为我们存放所有资源的根目录， 例如：myblog。
2. 在 myblog（后面的根目录也指 myblog目录）中新建一个 index.html 文件， 内容可以自由发挥。
	```xml
	<!doctype html>
	<html>
	  <head>
	    <meta charset="utf-8">
	    <title>My frist Post</title>
	  </head>
	  <body>
	    <h1>My frist Post</h1>
		<p>This is my first post with Jekyll.</p>
	  </body>
	</html>
	```
3. 开启命令行，在 myblog 目录下运行一下命令, 然后网站就起来了，可以访问 http://localhost:8080/ 就可以看到发布的 index.html 的内容。下面命令中 -P 是指定端口号，Jekyll 默认的端口号是 4000， 可是在我本机跑不起来，就指定了 8080。
```
jekyll serve -P 8080
```
