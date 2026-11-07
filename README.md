# KRIS — 品牌策略 · 内容表达 · 业务结果

个人作品集网站（静态站 + 源工程）。

线上预览：<https://554332044kris-cyber.github.io/kris-portfolio-1.2/>

---

## 仓库结构

```
.
├── index.html          # 静态站入口（单文件页面，样式与字体已内联）
├── assets/             # 站点素材
│   ├── cases/          # 案例配图 / 视频（webp / jpg / png / mp4）
│   ├── logos/          # 品牌墙 logo
│   └── media/          # AI 视频案例封面与视频
├── docs/CV.pdf         # 「下载简历」按钮指向的文件
├── robots.txt
├── sitemap.xml
└── source/             # React + Vite 源工程（改版用）
    ├── index.html
    ├── src/            # App.tsx / main.tsx / index.css / cases.json
    ├── public/assets/  # 构建时的静态资源目录
    ├── package.json
    ├── vite.config.ts
    └── tsconfig.json
```

## 页面板块

单页锚点导航：首屏 `#top` → 案例库 `#case-studies` → 素材 / AI 视频 `#case-media` → GTM 思维 `#gtm-thinking` → 联系我。

## 修改内容

**方式一（推荐，改文案/图片）**：直接编辑根目录 `index.html`，资源引用均为相对路径 `./assets/...`，替换同名文件即可。

**方式二（改结构/样式）**：进入 `source/` 目录

```bash
cd source
pnpm install     # 或 npm install
pnpm dev         # 本地开发
pnpm build       # 产物在 source/dist
```

源工程构建产物与根目录 `index.html` 为两套实现，确认无误后再手动替换根目录文件。

## 部署

GitHub Pages 从 `main` 分支根目录发布，推送即生效：

```bash
git add -A
git commit -m "Update content"
git push
```

文档中的 `sitemap.xml` / `robots.txt` 内域名如需指向新地址，请一并调整。
