---
layout: post
title: 从零搭建个人博客
date: 2026-10-10
excerpt: 记录用 Jekyll + GitHub Pages 把一个文件夹变成公开网站的过程。
tags:
  - 学习
---

今天把这个博客搭起来了。

整个流程其实并不复杂——不需要在本地安装 Ruby 或 Jekyll，只需要一个 Git 仓库和 GitHub Actions 就能自动构建发布。

## 搭建过程

1. 使用现成的 Jekyll 模板，克隆到本地
2. 修改 `_config.yml`，填入自己的名字和邮箱
3. 编辑 `index.html`，替换项目卡片和联系方式
4. 创建 GitHub 远程仓库，推送代码
5. 在仓库设置里打开 GitHub Pages，Source 选 GitHub Actions
6. 等待 workflow 跑完，博客就上线了

## 以后怎么写文章

在 `_posts/` 里新建一个文件，文件名格式是 `YYYY-MM-DD-title.md`，开头写好 Front Matter，之后直接写 Markdown 正文就行。

写完之后：

```
git add _posts/新文章.md
git commit -m "新增文章：标题"
git push
```

GitHub Actions 会自动重新构建并发布。

## 下一步

- 继续写文章
- 完善项目卡片里的内容
- 慢慢把想法整理出来
