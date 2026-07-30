# .emacs.d

一套专为 Racket 开发打造的精简 Emacs 配置。基于 `use-package` 构建，追求简洁——不依赖臃肿的框架，只保留干净高效编辑体验所需的核心配置。

![Emacs Lisp](https://img.shields.io/badge/Emacs_Lisp-7F5AB6?logo=gnuemacs&logoColor=white) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

[English](README.md) · **中文**

## 功能特性

- **Racket IDE** —— `racket-mode` 集成 REPL、XP 模式（自动补全）以及 paredit 结构化编辑
- **清爽界面** —— 无工具栏、无滚动条、无启动画面
- **现代化默认值** —— 条形光标、行号、自动配对、彩虹括号
- **Which-key** —— 屏幕提示，便于发现可用键绑定
- **注释切换** —— `C-c c` 一键注释/取消注释选区

## 环境要求

| 依赖 | 用途 / 版本 |
|------|------------|
| Emacs | 27+（已在 Emacs 29 上测试） |
| 网络连接 | 用于首次安装扩展包 |

## 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/turinglambdaai/.emacs.d.git ~/.emacs.d
```

### 2. 启动 Emacs

启动 Emacs，扩展包会在首次运行时自动安装。

## 扩展包

| 扩展包 | 用途 |
|---------|---------|
| `racket-mode` | Racket 主模式，集成 REPL（`C-c C-r` 发送选区、`C-c C-z` 打开 REPL） |
| `racket-xp` | 自动补全与行内错误检查 |
| `paredit` | S-表达式结构化编辑 |
| `which-key` | 交互式键绑定发现 |

## 使用

| 快捷键 | 功能 |
|----------|--------|
| `C-c c` | 注释/取消注释选区 |
| `C-c C-r` | 发送选区到 Racket REPL |
| `C-c C-z` | 打开 Racket REPL |

## 配置说明

本配置使用清华 MELPA 镜像以加速国内下载。如需切换为官方镜像，修改 `init.el` 中的 `package-archives`：

```elisp
(setq package-archives
      '(("melpa" . "https://melpa.org/packages/")
        ("gnu"   . "https://elpa.gnu.org/packages/")))
```

## 项目结构

```
.emacs.d/
├── init.el          # 入口，扩展包与模块配置
└── README.md        # 本文件
```

## 许可证

基于 [MIT License](LICENSE) 开源。
