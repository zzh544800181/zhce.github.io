---
title: hexo搭建及发布博客
date: 2018-05-05 21:32:27
tags:
---
 大家好，这篇文章主要讲述了如何通过hexo搭建一个属于自己的blog，写篇文章，并且发布到github上去。欢迎阅读~

## 必要的安装
- 安装git bash
> 下载windows版本的git bash安装及好，安装好通过`git version`查看版本
- 安装nodeJs
> hexo是基于nodeJs的静态博客，nodeJs有LTS(长期支持版)、Current(当前最新版)两个版本，最后安装好通过`node -v`查看版本
- 安装hexo
> 创建个文件夹存放hexo,通过执行命令 `npm i -g hexo`,安装完后`hexo -v`查看版本

## 进入到第二步——初始化
- 通过命令`hexo init`初始化
- 执行`hexo clean`、 `hexo generate`、`hexo server`
- 访问`http://localhost:4000`就可以看到自己的blog
- 访问`https://hexo.io/themes/`下载各种themes，找到喜欢的按照文档安装使用 

## 写文章
- 执行`hexo new '文章名'
- 进入到`source/_posts`路径下去就能看到新建的`'文章名'.md`的文本
- 采用md的方式写好自己的文章

## 发布文章
- 在`_config.yml`文件中修改参数，例如：
> deploy:
    type:git
- 执行`hexo deploy`发布