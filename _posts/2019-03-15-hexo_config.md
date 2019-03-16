---
layout: post
title: "hexo_config"
date: 2019-03-15
category: hexo
tags: hexo
---

## 前言：

为什么要用hexo，首先是因为gitalk 出现了一个Error: Validation Failed.问题，具体原因是gitalk 的id 有50个字符的限制，因为是用的pathname，然后pathname长度超了，然后去网上搜索问题，发现有的解决方法是要改成site.title,但是我有部分文章的title也是超长的，然后这个问题一直搁置了，后来我看到了一个hexo的持久化链接的文章，可以随机生成一个字符串作为持久化链接，是通过一个hexo-abbrlink的一个插件，我搜索了一下发现jekyll并没有这个插件，然后还发现了一些hexo的一些其他插件很好用，如hexo-admin，恩，就打算迁移到hexo。  

## hexo 初始化

在使用hexo之前你需要安装nodejs  

[nodejs官网](https://nodejs.org/en/)  
[hexo官网](https://hexo.io/zh-cn/)  

安装nodejs之后安装hexo  

	npm install hexo-cli -g
	hexo init blog
	cd blog
	npm install
	hexo server

## hexo 主题

[hexo theme](https://hexo.io/themes/)  

或者在github 上搜索 hexo theme找到你喜欢的主题  

这个是一个我比较喜欢的主题  
[aircloud github](https://github.com/aircloud/hexo-theme-aircloud)  
[aircloud](http://niexiaotao.cn/)  

	切换到博客目录
	mkdir themes/aircloud
	git clone https://github.com/aircloud/hexo-theme-aircloud.git themes/aircloud/

	aircloud 搜索功能
	npm i hexo-generator-search --save
	添加_config.yml
	search:
	  path: search.json
	  field: post

	修改_config.yml theme
	theme: aircloud

其他的一些配置参照[aircloud readme](https://github.com/aircloud/hexo-theme-aircloud/blob/master/readme.md)  

然后修改了一些地方，包括配置，头像，评论，文章之类的  

## jekyll命令

	hexo new <title>
	hexo generate 生成静态文件
	hexo clean 清理
	hexo publish <title> 草稿移动到 source/_posts (没有试过
	hexo server
	hexo deploy 部署到网站
	hexo new page tags 

## jekyll to hexo 

因为我之前的博客是jekyll 来的 迁移到hexo 有一些问题或者差异然后记录下  

## other hexo 

另外一些hexo的配置
