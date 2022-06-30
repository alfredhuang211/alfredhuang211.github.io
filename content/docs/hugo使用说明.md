---
title: "使用hugo构建内容输出的静态站点"
date: 2022-06-27
summary: "当前项目的 hugo 使用总结"
---


## hugo 安装

在 mac 中使用 brew 安装即可；

在 windows 中可以使用 chocolatery 来安装 hugo 和 hugo extend；

## hugo 打包项目

在项目下使用 hugo 命令完成编译打包，输出内容进行静态部署就可以了；

通过在 `config.toml` 中增加 `publishDir = "docs"` 指定输出到 docs 目录中，github pages 配置识别 docs 目录；如果不指定的情况下，默认输出到 public 目录；配置需注意引号；

# 使用技巧

## _index.md

内部需要有基础内容，作为每个目录的默认页


## 文件头

文件使用如下格式开头，用于 hugo 识别内容信息

```
---
title: "使用hugo构建内容输出的静态站点"
date: 2022-06-27
summary: "当前项目的 hugo 使用总结"
tags: []
featured_image: ""
---

```

