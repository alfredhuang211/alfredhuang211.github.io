---
title: "设置hugo静态站点的主题"

date: 2024-02-28

summary: "hugo的主题设置"

categories: "hugo"

tags: ["hugo"]

toc: true # 展示ToC

---

## 下载安装

hugo的站点主题，大部分都是可以直接下载后使用。当然，在使用时还是需要阅读主题的说明书。

一般来说，主题均是有对应的github项目仓库的。进入项目仓库后查看，如果是引导将项目添加为个人站点 theme 文件夹下的子项目的，那利用添加子项目或者直接下载 git 仓库均可以使用。

但是还是有部分主题不是使用这种方式，需要进行编译安装。这种主题一般需要根据仓库说明进行前端环境的配置和编译，或者直接下载项目的release，然后放置到个人站点的 themes 文件夹下。

目前项目采用的是 Mainroad 主题，项目地址 https://github.com/Vimux/Mainroad

## 配置使用

相对于安装，配置是使用主题更需要注意的一点。目前的主题配置也都是在项目的 config.toml 文件中。具体的配置参数需要根据主题的示例或说明进行。对于 hugo 来说，其实有些不友好的地方，就是主题配置和项目配置均混合在一起，导致比较难区分哪些配置是 hugo 本身使用，哪些是主题在使用。 

## 文章题头内容

针对文章来说，大部分的题头内容都差不多，例如 title，date，categories，tags，这些是hugo的标准定义的参数，但是主题也会有些自定义参数。如下例子是mainroad主题的题头例子，可以看到例子里面本身也区分为了 common-defined 和 theme-defined，就是标准定义参数还是主题所使用的参数。

```
---
# Common-Defined params
title: "Example article title"
date: "2017-08-21"
description: "Example article description"
categories:
  - "Category 1"
  - "Category 2"
tags:
  - "Test"
  - "Another test"
menu: main # Optional, add page to a menu. Options: main, side, footer

# Theme-Defined params
thumbnail: "img/placeholder.png" # Thumbnail image
lead: "Example lead - highlighted near the title" # Lead text
comments: false # Enable Disqus comments for specific page
authorbox: true # Enable authorbox for specific page
pager: true # Enable pager navigation (prev/next) for specific page
toc: true # Enable Table of Contents for specific page
mathjax: true # Enable MathJax for specific page
sidebar: "right" # Enable sidebar (on the right side) per page
widgets: # Enable sidebar widgets in given order per page
  - "search"
  - "recent"
  - "taglist"
---
```

### 文章 front matter 注意事项

* 时间问题：
日期时间格式可以匹配 config 文件中格式，月份需要是两位数，否则可能出现日期排序不正常现象。
