# Folder Hover Animation

A lightweight folder-opening hover animation built with plain HTML and CSS.  
一个使用原生 HTML 和 CSS 制作的轻量级文件夹悬浮打开动效。

![Preview](./assets/preview.svg)

## Overview | 项目简介

This project recreates a layered folder interaction using four PNG assets.  
这个项目使用 4 张 PNG 图层素材，组合出一个具有层次感的文件夹打开动画。

- Layer 1 acts as the base.  
  第 1 层作为底层。
- Layers 2 and 3 lift upward with a slight bounce.  
  第 2、3 层在悬浮时会上抬，并带一点回弹。
- Layer 4 flips outward on hover with its bottom edge fixed.  
  第 4 层在悬浮时以下边缘为轴向外翻开。

The project is dependency-free and can be opened directly in a browser.  
项目无依赖、无构建步骤，直接用浏览器打开即可运行。

## Features | 功能特点

- Pure HTML + CSS
- No build step
- Responsive layout
- 3D folder lid flip
- Staggered layer motion
- Easy to tune animation parameters

- 原生 HTML + CSS
- 无需打包构建
- 支持响应式布局
- 带 3D 文件夹翻盖效果
- 分层错峰动画
- 参数容易微调

## Demo | 预览方式

Open [index.html](./index.html) directly in your browser.  
直接在浏览器中打开 [index.html](./index.html) 即可预览。

If you publish this repository with GitHub Pages, it can also serve as the live demo page.  
如果发布到 GitHub Pages，这个页面也可以直接作为在线演示页。

## Project Structure | 项目结构

```text
.
├── assets/
│   ├── preview.svg
│   ├── 第一层.png
│   ├── 第二层.png
│   ├── 第三层.png
│   └── 第四层.png
├── index.html
├── LICENSE
├── CONTRIBUTING.md
├── commit-template.txt
└── README.md
```

## Animation Logic | 动画逻辑

The core interaction is defined in the CSS inside `index.html`.  
核心交互逻辑都写在 `index.html` 的 CSS 中。

- `.layer-2`: first inner sheet, lifts the farthest  
  `.layer-2`：第一张内部纸张，上抬幅度最大
- `.layer-3`: second inner sheet, starts after layer 2 begins moving  
  `.layer-3`：第二张内部纸张，在第 2 层启动后延迟开始运动
- `.layer-4`: folder cover, rotates on the X axis using the bottom edge as the hinge  
  `.layer-4`：文件夹盖板，以下边缘为铰链做 X 轴翻转
- `.folder`: provides `perspective` for the 3D opening effect  
  `.folder`：提供 3D 透视效果

## Customization | 可调参数

Edit the CSS in [index.html](./index.html) to tune the interaction:  
可以直接编辑 [index.html](./index.html) 中的 CSS 来调整动画：

- `.folder:hover .layer-2`: layer 2 lift distance  
  调整第 2 层上抬距离
- `.folder:hover .layer-3`: layer 3 lift distance and delay  
  调整第 3 层上抬距离与延迟
- `.folder:hover .layer-4`: folder lid opening angle  
  调整第 4 层翻盖角度
- `.folder`: `perspective` strength  
  调整 3D 透视强度
- `.layer-2, .layer-3`: easing curve  
  调整第 2、3 层的回弹节奏

## GitHub Pages | 发布到 GitHub Pages

1. Create a new GitHub repository.  
   创建一个新的 GitHub 仓库。
2. Push this folder to the repository root.  
   将当前目录内容推送到仓库根目录。
3. Open repository settings.  
   打开仓库设置。
4. Enable GitHub Pages from the default branch.  
   从默认分支启用 GitHub Pages。
5. Use the repository root as the source.  
   选择仓库根目录作为发布源。

## License | 许可证

MIT

## Author | 作者

yangshaoqiang

GitHub: [github.com/yangshaoqiang](https://github.com/yangshaoqiang)
