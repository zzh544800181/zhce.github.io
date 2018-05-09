---
title: hexo异地同步
date: 2018-05-09 23:48:44
tags:
---
 大家好，今天给大家讲下如何在两台电脑上同步更新你的博客~

## 拉取到本地
- 在github创建hexo分支
- 在setting中设置该分支为默认分支
- clone 项目到本地，通过`git branch -a`查看是否拉取到分支
- `cp`hexo下面全部文件到clone到本地的项目中，覆盖项目
## 同步到git
- 执行 `hexo c && hexo g &&hexo d`命令，接着去看是否能打开
- 如果blog正常运行，就可以执行
> `git add .`
> `git commit -m "add hexo settting"`
> `git push`
>  注意要在hexo分支下操作
>  这个时候，在origin上，hexo分支和master分支code不相同
-  在下次clone到本地后，运行`rm -rf .deploy_git`，将`.deploy_git`文件件删掉，否则会把整个项目部署到master分支
