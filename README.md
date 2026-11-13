# 口袋星期天 · 最终源码

本仓库提供可直接打开的最终游戏页面，以及完整的 HTML/CSS/JavaScript 源码和构建脚本。

## 打开游戏

1. 在本仓库点击 **Code → Download ZIP**，或[下载源码 ZIP](https://github.com/shiyirong0128/DS_WORK_FINAL/archive/refs/heads/main.zip)。
2. 解压下载的文件。
3. 双击根目录的 **index.html**，在启用 JavaScript 的现代浏览器中游玩。

无需安装 Node.js、无需服务器，也无需联网。首页已内嵌样式、脚本、字体和图形；单独复制 `index.html` 也能打开。

GitHub 的文件页用于查看源代码。要运行游戏，请下载后打开 `index.html`，不要把 GitHub 上的源码预览当作游戏页面。

## 操作与功能

| 操作 | 键盘 | 页面按钮 |
| --- | --- | --- |
| 移动 | 方向键或 W / A / S / D | 十字方向键 |
| 撤销 | Z 或 Backspace | ↶ |
| 重开 | R | ↻ |

关卡为可解的 7×7 地图，含 5 个箱子和 5 个目标点。有效移动计步，推动箱子另计推动次数；撞墙或箱子被挡住时不改变位置与计数，并显示短暂回弹和“Oops推不动了”提示。撤销恢复上一有效状态，重开归零，通关页显示本局真实成绩。

保留 WASD/方向键与屏幕按键同步反馈、到位箱子的像素勾、角色脚下的目标标记，以及键盘焦点框和短窗口中的焦点滚动修复。

## 文件说明

| 文件或目录 | 用途 |
| --- | --- |
| `index.html` | 正式入口；内含游戏与通关界面，可直接离线打开 |
| `complete.html` | 转到同目录首页的实际通关结果；没有通关记录时显示待挑战状态 |
| `partial.html` / `solved.html` | 当前风格的静态状态参考，不在正式页面导航中 |
| `src/pocket.css` | 页面样式源码 |
| `src/runtime.js` | 键盘、按钮、反馈、渲染和焦点交互源码 |
| `src/game.mjs` | 移动、阻挡、计数、撤销、重开和通关规则 |
| `src/boards.mjs` | 地图、初始局面和静态参考数据 |
| `scripts/build.mjs` | 从源码生成根目录 HTML |
| `scripts/preview.mjs` | 可选的本地预览服务 |
| `scripts/browser.mjs` / `scripts/capture.mjs` | 浏览器验证与截图工具 |
| `tests/` | 规则测试与浏览器检查辅助代码 |
| `assets/fonts/` | 内嵌像素字体及 SIL Open Font License |
| `预览图/` | 最终设计方向的预览图 |
| `SOURCE.json` | 最终版来源仓库、提交与阶段记录 |

## 修改和重新构建

仅开发或测试时需要 Node.js。修改 `src/` 或 `scripts/build.mjs` 后，在仓库根目录运行：

```sh
node scripts/build.mjs
node --test tests/game.test.mjs
```

无需 npm 安装。可选预览：

```sh
node scripts/preview.mjs
```

然后访问 `http://127.0.0.1:4173/`，结束时按 Ctrl+C。

截图工具使用 Node.js 22+ 和本机 Chrome；可通过 `CHROME_PATH` 指定浏览器，然后运行 `node scripts/capture.mjs`。截图工具属于开发辅助，打开游戏不需要它。

## 版本来源

本次交付的页面、源码及测试文件来自 [DS_WORK2 的 07_Skill审查与修复](https://github.com/shiyirong0128/DS_WORK2/commit/61010c9105ede2b66d2e466eef3678f8b7e19aae)。先前方案与审查历史保留在原开发仓库，本仓库单独提供最终页面源码。
