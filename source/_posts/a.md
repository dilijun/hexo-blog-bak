---
title: Hexo搭建博客（初级篇）
tags: [hexo,github]
category: hexo
comments: true
---
Hexo 是一个基于Node.js的快速、简洁且高效的博客框架。使用Markdown来编写文章，利用靓丽的主题可快速、轻松生成静态网页。
<!-- more -->

### 环境准备
在安装Hexo之前，我们必须保证已安装一下应用程序：
* Node.js
* Git
1. 安装Node.js（如已安装，可忽略该步骤）
下载地址：[Node.js](https://nodejs.org/en/download/)
安装成功后使用以下命令测试是否安装成功：
`node -v`
2. 安装Git（如已安装，可忽略该步骤）
下载地址：[Git](https://git-scm.com/downloads) 
安装成功后使用以下命令测试是否安装成功：
`git --version`
### 搭建博客
1. 安装hexo，命令：
`npm install -g hexo-cli`
2. 初始化博客，命令：
```
hexo init <blog_name> --<blog_name>为你自己博客项目的名称，或者可以 mkdir <blog_name>，进入该目录下执行 hexo init
cd <blog_name>
npm install
```
3. 博客初始化后，可以使用以下命令启动博客：
```
hexo clean --清除缓存文件 (db.json) 和已生成的静态文件 (public)
hexo g(hexo generate) --生成静态页面 
hexo s(hexo server) --开启本地服务
```
4. 此时打开浏览器，访问 http://localhost:4000 即可看到自带默认主题的博客。
![](http://pgnau40bx.bkt.clouddn.com/%E5%88%9D%E5%A7%8B%E5%8D%9A%E5%AE%A2.jpeg)

5. Hexo命令知多少
```
hexo help --可查看hexo命令
hexo generate --生成博客静态页面，也可用缩写命令 hexo g
hexo clean --清除生成的静态页面
hexo server --开启本地服务，也可用缩写命令 hexo s、hexo server --debug 是开启debug模式
hexo deploy --部署博客，也可用缩写命令 hexo d
hexo new 'postName' --新建文章，默认会在 source/_posts/ 下生成<postName>.md的Markdown文件
hexo new page 'pageName' --新建页面，默认会在 source目录下，生成<pageName>文件夹，并在该文件夹下生成 index.md 文件
```
### 博客上github
1. 确保有github账号，没有的可自己去申请。
2. 创建代码库，命名规则为`yourname.github.io`，‘yourname’为你自己github的用户名。
![enter description here](http://pgnau40bx.bkt.clouddn.com/github%E5%88%9B%E5%BB%BA%E4%BB%A3%E7%A0%81%E5%BA%93.jpeg)
3. 生成ssh keys
`ssh-keygen -t rsa -C "your_email@example.com"`，一路回车即可，创建成功后，会在用户目录下的 .ssh 目录下生成 id_rsa和id_rsa.pub两个文件，我们把id_rsa.pub中的内容拷贝到github上即可，title可以随便填写。
![enter description here](http://pgnau40bx.bkt.clouddn.com/github%E9%85%8D%E7%BD%AEssh_key.jpeg)
配置好后，可以使用`ssh -T git@github.com`命令来测试是否配置成功。

