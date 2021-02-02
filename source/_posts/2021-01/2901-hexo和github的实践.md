---
title: 建站第一篇，这个博客的由来
urlname: 建站第一篇，这个博客的由来
tags:
  - 杂谈
categories:
  - 杂谈
description: 附加一段文章摘要，字数最好在140字以内，会出现在meta的description里面
top: true
date: 2021-01-29-001
abbrlink: 27bfeede
---

## Hexo + github 建立个人博客
        原本是通过阿里云服务器，让后端朋友写了后端的增删改查服务，然后自己写页面来搭建了自己的个人网站。
        但是个人服务器的带宽太小，一些图片加载太慢了，导致整个网站的速度极其卡顿，一点都不想打开，所以考虑通过现有的博客搭建，只专注内容就好了。
        最后选择Hexo建博客，也只是试试，如果以后有更好的选择，也许就换掉了。
<!-- more -->
## 通过Hexo搭建
1. 因为以前做过node.js的开发，所以npm相关都是齐全的，不用再安装了，但是需要升级，不过电脑上的其他项目，npm的版本也会有影响，所以升级前要注意这个问题：

    升级npm：`npm install -g npm`  
    升级至指定版本：`npm -g install npm@6.8.0`  
2. 通过npm安装Hexo:  `npm install -g hexo-cli`
3. 在当前路径下，创建名为‘blog’的Hexo项目文件夹：`hexo init blog` 
4. 进入‘blog’文件夹：`cd blog` 
5. 安装依赖： `npm install` 

    安装完成后项目结构为：
    - node_modules: 依赖包（通过执行 `npm install` 命令，产生的文件夹）
    - public：存放生成的页面（后续环节中通个 `hexo g` 命令生成）
    - scaffolds：生成文章的一些模板
    - source：用来存放你的文章（默认文章为`.md`结尾的Markdown格式的文件，存放于当前文件夹下的`_posts`文件夹中）
    - themes：主题
    - _config.yml: 博客的配置文件
    - 其他文件就不要乱动了 

6. 将当前的代码文件打包：`hexo g` （会生成‘public’文件夹）
7. 开启Hexo服务：`hexo s` (可在本地访问：http://localhost:4000)
----------
## github的仓库
1. 在github上创建一个空的公开仓库
2. 将仓库的地址，放在当前项目文件夹下`_config.yml`中（/blog/_config.yml）

----------
## 再开发时候的操作
1. git clone 代码 
2. npm install 
3. 安装主题：npm install --save hexo-renderer-pug 
4. 安装git：npm install hexo-deployer-git --save 
5. 执行 hexo g 生成编译文件 
6. 执行 hexo d 上传编译文件

----------
## 小结
    好麻烦啊。。。。所说个性化定制挺好的，但是各种要配置的，主题也是，看起来怪怪的，写的文章，超链接什么的也不好弄。。。[苦涩]