---
title: "使用hugo构建静态站点"

date: 2022-06-27

summary: "当前项目的 hugo 使用总结"

categories: "hugo"

tags: ["hugo"]

toc: true # 展示ToC

---


# 使用hugo构建静态站点

### hugo 安装

在 mac 中使用 brew 安装即可；

在 windows 中可以使用 chocolatery 来安装 hugo 和 hugo extend；

也可以直接在 hugo 项目 release中下载二进制包直接使用；

### hugo 打包项目

在项目下使用 hugo 命令完成编译打包，输出内容进行静态部署就可以了；

通过在 config.toml 中增加 publishDir = "docs" 指定输出到 docs 目录中，github pages 配置识别 docs 目录；如果不指定的情况下，默认输出到 public 目录；配置需注意引号；

### hugo or hugo-extend

hugo-extend额外支持了SASS/SCSS，这个能力是有些主题所依赖的，目前可以在没有特殊情况时，均使用extend里面的可执行文件hugo命令来执行。

## 使用技巧

### _index.md

内部需要有基础内容，作为每个目录的默认页

### 文件头

文件使用如下格式开头，用于 hugo 识别内容信息
```
---
title: "使用hugo构建内容输出的静态站点"

date: 2022-06-27  
lastmod: 2018-12-08T15:26:15Z   # 最近修改
publishdate: 2018-11-23T15:26:15Z  # 发布时间

summary: "当前项目的 hugo 使用总结"

tags: []

featured_image: ""  #应该是题图
images:
    - images/pexels-photo-196666.jpeg #图片？

draft: false  # true or false，告知是否是草稿？是否需要发布？

weight: 20    # 展示权重

TableOfContents: true # 展示ToC

featured_image: ""
---
```

### 主题

主题均放在项目根目录的 themes 文件夹下；

不同主题有不同使用方法，要注意主题的说明文档；

### 目录结构

每个目录下的_index.md，带有的title，可以在后续文章上呈现。

## 待解决 TODOList

### 首页最近文档

目前始终未对齐最新文档，看起来局限在了某个目录下。