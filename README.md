# AI探索手稿 · 阿花的试验田

阿花的 AI 探索之旅：感想记录、工具开发。站点地址：<https://gardenwpy.github.io/AIexplorer/>

## 每周更新（推荐方式）

1. 在本对话里直接发文字，草稿、语音转写、零散要点都行。
2. 我会整理成 Markdown 文章，生成本地预览给你看。
3. 你确认后，我推送到本仓库 `main` 分支，GitHub Pages 自动更新。

## 自己更新（GitHub 网页版）

1. 打开仓库 → `Add file` → `Create new file`。
2. 文件名：`_posts/YYYY-MM-DD-英文短名.md`，例如 `_posts/2026-11-27-first-post.md`。
3. 填入下面的模板，点 `Commit changes`。

## 文章模板

```markdown
---
layout: post
title: "文章标题"
date: 2026-11-27
category: 工具实测
tags: [标签1, 标签2]
---

## 问题
想解决什么？

## 尝试
做了哪些事？

## 结果
发生了什么？

## 收获
下次怎么改？
```

`category` 六选一：`探索时间线` / `项目复盘` / `工具实测` / `学习笔记` / `实验日志` / `资源清单`。

## 本地结构

- `_posts/`：文章（Markdown）
- `_layouts/`：页面模板（含 `timeline.html`）
- `_includes/`：页头、页脚、天空（`sky.html`：全站页顶单层淡蓝起伏 + 6 朵错落白云，部分重叠更浓白，不占空间）、花朵效果（`effects.html`：全站鼠标跟随花朵 + 点击散花）、草地（`garden.html`：全站页面底部双层起伏草丘 + 16px 小花，花随鼠标方向倾斜，不占空间）、阅读进度条（`progress.html`：顶部粉色细线随滚动填充）、飘落花瓣（`petals.html`：每 1–2 分钟 1–2 片半透明粉花瓣从右上翻滚飘落，随机消失于左侧/左下角/底边）
- `assets/css/style.css`：样式
- `about.md`：关于页
- 首页开关（`toggle.html`：仅首页、「阿花的试验田」下方，一个滑动开关同时控制鼠标跟随、点击散花、花瓣飘落，状态存浏览器本地，刷新后保留）
- `timeline.md`：时间轴页（方案 4 · 年份分组），地址 `/timeline/`
- `preview.html`、`timeline-options.html`、`timeline-preview.html`、`garden-options.html`、`article-preview.html`：**仅本地预览用，不推送**（已在 `_config.yml` 中排除）

## 发布

仓库 Settings → Pages → Source 选 `main / root`，已开启。推送后约 1 分钟生效。
