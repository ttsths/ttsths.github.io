---
cover: ""
category: ""
tags:
  - blog
status: 已发布
date: "2023-09-28 16:49:00"
catalog:
  - blog
urlname: hexo-blog-CI
title: 个人博客最优实践
summary: ""
sort: ""
updated: "2023-10-11 16:47:00"
---

使用 Notion 记录文章，markdown 格式

github action 自动同步 notion 文章，并推送 Telegram

本地使用

使用 hexo 搭建静态

hexo 极简主题

- [hexo-theme-minimalism](https://github.com/f-dong/hexo-theme-minimalism)
- [hexo-theme-organes](https://github.com/zchengsite/hexo-theme-oranges)

基于[MongoDB](https://cloud.mongodb.com/v2/65263a9d000bc537a98a13b8#/clusters/connect?clusterId=Cluster0)和[verche](https://vercel.com/ttsths/hexo-twikoo/Ct1KjskocSG3AC2K3sY4L7BSaJPm)的的[twikoo](https://twikoo.js.org/backend.html#vercel-%E9%83%A8%E7%BD%B2)评论系统(白嫖

[mongoDB URL](mailto:sin2%3Dcos2%3D1@cluster0.irspyaq.mongodb.net)

verche app: [https://vercel.com/ttsths/hexo-twikoo/Ct1KjskocSG3AC2K3sY4L7BSaJPm](https://vercel.com/ttsths/hexo-twikoo/Ct1KjskocSG3AC2K3sY4L7BSaJPm)

## elog

[Elog](<[https://elog.1874.cool/notion/start](https://elog.1874.cool/notion/start)>)基于 Node，用于将 Notion 作为数据库将 blog 部署到 github page 并在多端同步

```bash
elog clean
elog sync -e .elog.env
```
