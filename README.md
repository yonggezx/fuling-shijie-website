# 🦊 浮灵饰界 · 官网

> 浮灵饰界（原 AI 龙虾）智能桌面宠物助手的官方网站：纯静态页面，无构建步骤，改动即生效。

![site](https://img.shields.io/badge/site-GitHub%20Pages-2ea44f)

![stack](https://img.shields.io/badge/stack-HTML5%20%7C%20CSS3%20%7C%20JS-lightgrey)

![version](https://img.shields.io/badge/version-1.0.12-blue)

![license](https://img.shields.io/badge/license-MIT-green)

🔗 线上地址：<https://yonggezx.github.io/fuling-shijie-website/>

---

## 📑 目录

- [📁 目录结构](#-目录结构)
- [🚀 本地预览](#-本地预览)
- [🔄 版本与下载链接同步](#-版本与下载链接同步)
- [🌐 部署](#-部署)
- [🔗 相关仓库](#-相关仓库)
- [📜 许可证](#-许可证)

---

## 📁 目录结构

```
.
├── index.html          # 官网首页（单文件，样式与脚本内联）
├── images/             # 应用截图与品牌图（由主仓库脚本自动采集）
│   ├── main-window.png
│   ├── ai-chat.png
│   ├── pet-window.png
│   ├── settings.png
│   └── ...
└── README.md
```

---

## 🚀 本地预览

页面无需依赖与构建，直接打开或用任意静态服务器查看：

```bash
# 方式一：浏览器直接打开
start index.html        # Windows
open index.html         # macOS

# 方式二：起一个本地静态服务（推荐，避免相对路径限制）
npx serve .
```

---

## 🔄 版本与下载链接同步

下载按钮指向 GitHub Releases 的最新安装包，产物名与主仓库 `package.json` 中的 `artifactName` 保持一致：

| 平台 | 产物名格式 |
| --- | --- |
| Windows | `FulingShijie-Setup-v{版本}.exe` |
| macOS | `FulingShijie-v{版本}-{arch}.dmg` |
| Linux | `FulingShijie-v{版本}.AppImage` / `.deb` |

发布新版本后，主仓库会自动执行 `scripts/sync-website-version.js`：脚本读取本次 Release 的真实资产名回填链接，并同步页面版本号与图片缓存戳，避免出现「链接指向不存在文件」的 404。

如需手动同步：

```bash
node scripts/sync-website-version.js --version=v1.0.12 --path=website/index.html
```

---

## 🌐 部署

推送 `main` 分支即触发 GitHub Pages 自动构建（通常 1 分钟内生效）。

> 注意：Pages 与浏览器会缓存静态资源约 10 分钟。截图、图标带 `?v=` 缓存戳，同步脚本会在每次发版时自动更新。

---

## 🔗 相关仓库

- 主仓库（源码 / Releases）：[fuling-shijie-update](https://github.com/yonggezx/fuling-shijie-update)
- 官网线上地址：<https://yonggezx.github.io/fuling-shijie-website/>

---

## 📜 许可证

本项目基于 [MIT 许可证](https://github.com/yonggezx/fuling-shijie-update/blob/master/LICENSE) 开源，© 2026 浮灵饰界。
