---
date: "2025-03-02T14:07:04+01:00"
draft: false
title: "在 Mac 下使用 Hugo 写 Blog 的安装与部署"
tags:
  - hugo
  - first categories
categories:
  - General
---

本文介绍如何在 Mac 上安装 Hugo、编写博客并部署到 GitHub Pages，整个过程简单易懂。

## 一. 环境准备与安装

**A. 安装 Hugo**

```bash
brew install hugo
```

**B. 创建站点**

1. 新建 Hugo 站点（使用 YAML 格式配置）

```bash
hugo new site wctd_blog --format yaml
```

2. 初始化 Git 仓库

```bash
git init
```

**C. 配置主题**

1. 添加 PaperMod 主题

```bash
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/hugo-PaperMod

```

## 二. 编写 blog 与预览

**A. 创建要写的文章**

```
hugo new posts/first-post.md

```

**B. 编辑博客内容**

使用编辑器（vim 或 VSCode）编辑文章

```bash
vim posts/first-post.md

```

**C. 本地预览**

启动本地服务器查看效果

```bash
hugo server -D

```

## 三. 部署与发布

**A. GitHub 仓库配置**

1. 添加远程仓库

```bash
git remote add origin https://github.com/oooshuang/blog.git

```

**B. GitHub Pages 设置**

1. 登录 GitHub，进入 blog 仓库
2. 进入 Settings → Pages 页面
3. 选择 Source 为 GitHub Actions
4. 配置 Hugo 工作流，确保 HUGO_VERSION 与本地版本一致

**C. 发布与访问**

1. 推送到 GitHub 仓库

```bash
git push -u origin main
```

2. 访问博客
   完成部署后，通过以下链接访问：
   https://oooshuang.github.io/blog/posts/first-post/
