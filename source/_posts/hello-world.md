---
title: Hexo博客使用说明
date: 3000-01-01 00:00:00
---

### 0. 最简单直接的使用方式

在`source/_posts`目录下放入md文件，在头部添加必要的`front-matter`信息
，例如：
```
---
title: Hexo博客使用说明
date: 2020-01-08 18:53:59
---
```
然后commit+push代码。

站点会在push后自动部署，等待一段时间刷新网页即可。


### 1. 安装依赖

```bash
yarn install
```

### 2. 编写新文章

``` bash
hexo new "文章标题"
```

通过命令创建文章，会自动根据`scaffolds`目录下的模板新建md文件，其中可以包含一些动态生成的信息，比如创建文章的时间。

### 3. 调试和预览

``` bash
$ hexo server
```

启动后访问`http://localhost:4000`即可本地预览

### 4. 常用功能

#### 分类与标签

在`Front-matter`中填写，比如
```
---
title: 这是一个标题
date: 2020-01-08 22:52:13
categories:
    - [前端, 移动端]
    - [前端, PC端]
    - [算法]
tags:
    - Vue
    - React
    - 递归
    - 算法
---
```
注意分类`category`和标签`tag`的区别，后者类似关键字。

详情参考：[https://hexo.io/zh-cn/docs/front-matter](https://hexo.io/zh-cn/docs/front-matter)

#### 插入本地图片

在`source/_posts`目录下创建与当前文章同名的文件夹，在其中放入图片等附件。

然后在md文档中插入以下代码即可显示存放在站点的本地图片。

```
{% asset_img 1.png %}
```

详情参考：[https://hexo.io/zh-cn/docs/asset-folders](https://hexo.io/zh-cn/docs/asset-folders)


#### 插入codepen在线代码

参考[https://github.com/bibixx/hexo-tag-codepen#usage](https://github.com/bibixx/hexo-tag-codepen#usage)



更多高级应用请查看[Hexo中文文档](https://hexo.io/zh-cn/docs/writing)