---
date: "2025-03-02T14:07:04+01:00"
draft: false
title: "在mac下使用 hugo 写 blog 的安装部署"
tags:
  - hugo
  - first
categories:
  - General
---

# 在 mac 下使用 hugo 写 blog 的安装部署

## mac 安装

brew install hugo

hugo new site wctd_blog --format yaml

git init

git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/hugo-PaperMod

hugo new posts/first-post.md

## 撰写 blog

vim posts/first-post.md

### 本地预览

hugo server -D

### 设置 github 远程仓库

git remote add origin https://github.com/oooshuang/blog.git

### 配置 GitHub Pages

登录 GitHub，进入仓库 Settings → Pages，确认 Pages 来源为 gh-pages 分支。完成后，你的博客将会自动通过 GitHub Actions 构建并发布，访问地址通常为 https://oooshuang.github.io/blog/。

### 推送到 github 仓库

git push -u origin main
