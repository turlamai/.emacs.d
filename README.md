# .emacs.d

A minimal Emacs configuration tailored for Racket development. Built on `use-package` with a focus on simplicity — no bloated frameworks, just the essentials for a clean and productive editing experience.

![Emacs Lisp](https://img.shields.io/badge/Emacs_Lisp-7F5AB6?logo=gnuemacs&logoColor=white) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

**English** · [中文](README.zh-CN.md)

## Features

- **Racket IDE** — `racket-mode` with REPL integration, XP mode (auto-completion), and paredit for structural editing
- **Clean UI** — no toolbar, no scrollbar, no startup screen
- **Modern defaults** — bar cursor, line numbers, electric pairs, rainbow parentheses
- **Which-key** — discoverable keybindings with on-screen hints
- **Comment toggle** — `C-c c` to comment/uncomment regions

## Requirements

| Dependency | Purpose / Version |
|------------|-------------------|
| Emacs | 27+ (tested with Emacs 29) |
| Internet connection | For initial package installation |

## Quick Start

### 1. Clone

```bash
git clone https://github.com/turinglambdaai/.emacs.d.git ~/.emacs.d
```

### 2. Launch Emacs

Launch Emacs. Packages are installed automatically on first run.

## Packages

| Package | Purpose |
|---------|---------|
| `racket-mode` | Racket major mode with REPL (`C-c C-r` send region, `C-c C-z` open REPL) |
| `racket-xp` | Auto-completion and inline error checking |
| `paredit` | Structural editing for S-expressions |
| `which-key` | Interactive keybinding discovery |

## Usage

| Shortcut | Action |
|----------|--------|
| `C-c c` | Comment/uncomment region |
| `C-c C-r` | Send region to Racket REPL |
| `C-c C-z` | Open Racket REPL |

## Configuration

This config uses the Tsinghua MELPA mirror for faster downloads in China. To switch to the official mirror, edit the `package-archives` in `init.el`:

```elisp
(setq package-archives
      '(("melpa" . "https://melpa.org/packages/")
        ("gnu"   . "https://elpa.gnu.org/packages/")))
```

## Project Structure

```
.emacs.d/
├── init.el          # Entry point, package and module configuration
└── README.md        # This file
```

## License

Licensed under the [MIT License](LICENSE).
