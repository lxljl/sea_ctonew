---
title: Hexo + Vue 天气站说明
---
欢迎来到广州天气观察小站！本站采用 Hexo 构建静态页面，并通过 Vue 在首页展示广州今日天气概览，提供清爽的交互式体验。

## 功能亮点

- **Vue 驱动的首页天气卡片**：使用 Vue 3 的 CDN 版本渲染天气数据，可轻松扩展为实时接口。
- **Hexo 静态生成**：快速生成静态页面，方便部署到 GitHub Pages。
- **清晰的结构**：首页聚焦天气信息，博客文章统一移动到 `/blog` 路径，方便后续扩展内容。

## 本地预览

```bash
npm install
npm run server
```

Hexo 默认会在 `http://localhost:4000` 启动预览服务，支持热更新。

## 发布到 GitHub Pages

在 `_config.yml` 中填写自己的 GitHub 仓库地址后运行：

```bash
npm run deploy
```

Hexo 会自动将生成的静态文件推送到 `gh-pages` 分支，实现一键部署。

祝使用愉快，也欢迎为本站补充更多的天气资讯！
