# AGENTS.md

## 项目概览
Notepad++ 中文官网仿站项目，使用纯 HTML + CSS 实现，无 JavaScript 框架依赖。

## 技术栈
- HTML5 + CSS3
- 原生 JavaScript（仅用于 Tab 切换和移动端菜单）
- Python HTTP Server（开发和部署服务）

## 文件结构
```
├── index.html          # 首页
├── download.html       # 下载页
├── features.html       # 功能特性页
├── versions.html       # 版本介绍页
├── tutorials.html      # 使用教程页
├── styles/
│   └── main.css        # 共享样式表
├── DESIGN.md           # 设计规范
├── AGENTS.md           # 本文件
└── .coze               # 项目配置
```

## 设计规范
- 主色：#6AB04C / #90BE6D（品牌绿）
- 强调色：#27AE60
- 背景白：#FFFFFF，区块浅灰：#F8FAFB
- 卡片圆角：12px，微阴影
- 字体：系统字体栈 + Noto Sans SC
- 详见 DESIGN.md

## 构建与运行
- 开发：`python -m http.server 5000 --bind 0.0.0.0`
- 无构建步骤，纯静态文件

## 代码风格
- HTML 语义化标签
- CSS 使用 CSS 变量（:root 定义）
- 响应式设计：768px / 480px 断点
- 组件化 CSS 类名（.card, .btn, .section 等）

## 注意事项
- 所有页面共享 styles/main.css
- 导航栏在所有页面中保持一致
- Tab 切换使用原生 JS，通过 data-tab 属性关联
- 移动端菜单使用 #navToggle 按钮切换
