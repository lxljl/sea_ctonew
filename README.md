# 广州天气观察 · Hexo + Vue

一个使用 [Hexo](https://hexo.io/) 构建、通过 Vue 展示天气信息的示例项目，可直接部署到 GitHub Pages，向用户提供广州今日天气状况。

## 在线访问

GitHub Pages 已启用，可通过以下地址访问站点：
- https://lxljl.github.io/sea_ctonew/

## 功能概览

- 📌 **Vue 驱动的天气卡片**：在首页以交互的方式展示广州今日温度、湿度与风力等数据。
- 🏗️ **Hexo 静态站点生成**：结构清晰，默认主题即刻可用，并将博客文章集中于 `/blog` 路径。
- 🚀 **GitHub Pages 部署支持**：集成 `hexo-deployer-git`，一条命令即可部署。

## 开发环境要求

- [Node.js](https://nodejs.org/) 16 或更高版本
- npm（随 Node.js 安装）

## 快速开始

```bash
npm install
npm run server
```

或使用 Yarn：

```bash
yarn install
yarn server
```

Hexo 会在 `http://localhost:4000` 启动预览服务，文件保存后页面会自动更新。

## 构建与部署

1. 如需部署到你自己的仓库，可编辑 `_config.yml` 更新 GitHub 信息。当前仓库的默认配置如下：
   ```yaml
   url: https://lxljl.github.io/sea_ctonew/
   root: /sea_ctonew/
   deploy:
     type: git
     repo: https://github.com/lxljl/sea_ctonew.git
     branch: gh-pages
   ```
   > 如果你 fork 了此项目，请将其中的用户名与仓库名替换为你自己的；也可以改为 `https://github.com/<用户名>/<仓库名>.git` 或 SSH 地址。

2. 构建并发布：
   ```bash
   npm run build   # 生成静态文件到 public/
   npm run deploy  # 将 public/ 推送到 gh-pages 分支
   ```

部署完成后，启用 GitHub Pages（`Settings -> Pages`）并选择 `gh-pages` 分支即可访问你的站点。

## 自定义天气内容

- 首页天气卡片的文案在 `source/index.md` 中维护，使用 Vue 3 的 CDN 版本渲染数据。
- 你可以直接修改其中的 `temperature`、`humidity` 等字段，或改造成从真实天气 API 拉取数据。
- 新增文章时执行 `npx hexo new post "文章标题"`，生成的文章默认会显示在 `/blog` 页面。

## 常用脚本

| 命令             | 说明                         |
|-----------------|------------------------------|
| `npm run server` | 启动本地预览（默认端口 4000） |
| `npm run build`  | 生成静态文件到 `public/`      |
| `npm run deploy` | 构建并推送到 GitHub Pages     |
| `npm run clean`  | 清理 `public/` 与缓存         |

## 许可证

本项目示例代码可自由拓展，欢迎在此基础上打造属于你自己的天气信息站点。
