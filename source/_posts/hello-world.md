---
title: Hexo博客使用说明
date: 3000-01-01 00:00:00
---

基于Hexo搭建的技术博客平台，相较于旧平台，主要有以下特性和改进：

- 使用Git项目形式管理博客，将md文件提交到服务器即可自动部署
- 支持本地预览
- 支持分页
- 支持使用分类和标签对文章进行归类
- 无后台的搜索功能
- 无后台的评论系统
- 支持引用本地图片避免外链
- 支持引入`codepen`、`codesandbox`、`jsfiddle`等在线代码
- 访客统计等更多丰富的插件和扩展能力

### ☯. 最简单直接的写文章方式

无需下载项目到本地，直接打开github项目地址：

[https://github.com/sishuguojixuefu/blog/new/master/source/_posts](https://github.com/sishuguojixuefu/blog/new/master/source/_posts)

创建md文件并保存，完毕。

注意在md文件头部添加必要的[`front-matter`](https://hexo.io/zh-cn/docs/front-matter)信息
，例如：
```
---
title: Hexo博客使用说明
date: 2020-01-08 18:53:59
---
```

站点会在push后自动部署，等待一段时间刷新网页即可。

### 1. 下载项目到本地，安装依赖

```bash
git clone https://github.com/sishuguojixuefu/blog.git blog
yarn install
```

### 2. 编写新文章

``` bash
hexo new "文章标题"
```

通过命令创建文章，会自动根据`scaffolds`目录下的模板新建md文件。

文件开头的[`front-matter`](https://hexo.io/zh-cn/docs/front-matter)默认包含了一些动态生成的信息，比如文章的标题和时间。

### 3. 调试和预览

``` bash
$ hexo server
```

启动后访问`http://localhost:4000`即可本地预览

### 4. 常用功能

#### 分类与标签

在[`front-matter`](https://hexo.io/zh-cn/docs/front-matter)中填写，比如
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

### 进阶使用

更多高级应用请查看[Hexo中文文档](https://hexo.io/zh-cn/docs/writing)