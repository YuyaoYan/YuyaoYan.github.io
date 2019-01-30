---
title: Hexo Quick Start
date: 2018-11-29
tags: hexo
cover: /img/post-cover/2.jpg
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)

### 新建导航栏文件夹

新建好后会自带`index.md`文件

``` bash
$ hexo new page categories
```

### 安装search

```bash
$ npm install hexo-generator-searchd --save
$ npm install hexo-generator-searchdb --save
```

### 上传本地图片的插件
在你的hexo目录下执行这样一句话
```bash
$ npm install hexo-asset-image --save
```

### 新建.md文档
新建后会在`_post`文件夹中产生同名文件夹。
```bash
$ hexo n "xxx"
```

`xxx`为`xxx.md`，执行该操作后产生`xxx`文件，该文件用来存放`xxx.md`中的图片。

### hexo常用命令
参见[大佬博客](https://blog.csdn.net/qq_26975307/article/details/62447489)

```bash
$ hexo n "我的博客" == hexo new "我的博客" #新建文章
$ hexo p == hexo publish
$ hexo g == hexo generate   #生成
$ hexo s == hexo server     #启动服务预览
$ hexo d == hexo deploy     #部署
```

### 每次部署时依次执行
```
hexo clean

hexo g

```

然后在浏览器打开  localhost:4000  看下效果，如果没有问题的话，就执行以下命令，部署到网站。

```
hexo d
```









