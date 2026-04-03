# Bruce's Ghostty Config

我的 Ghostty 终端配置文件，专为 Claude Code 优化。

## 主要特性

- **零报错** - 稳定可靠的配置
- **左右分屏** - `Cmd + D` 新增右侧分屏
- **一键缩放** - `Cmd + Shift + Enter` 或 `Cmd + Shift + F` 切换分屏缩放
- **半透明背景** - 85% 透明度，30px 模糊半径
- **Catppuccin Mocha 主题** - 护眼的深色主题

## 快捷键

| 快捷键 | 功能 |
|--------|------|
| `Cmd + D` | 新增右侧分屏 |
| `Cmd + Shift + Enter` | 切换分屏缩放 |
| `Cmd + Shift + F` | 切换分屏缩放 |
| `Cmd + Shift + ,` | 重载配置 |

## 配置内容

```ghostty
# --- Typography ---
font-family = "Maple Mono NF CN"
font-size = 14
adjust-cell-height = 2

# --- Theme and Colors ---
theme = Catppuccin Mocha

# --- Window and Appearance ---
background-opacity = 0.85
background-blur-radius = 30
macos-titlebar-style = transparent
window-padding-x = 10
window-padding-y = 8
window-save-state = always
window-theme = auto

# --- Cursor ---
cursor-style = bar
cursor-style-blink = true
cursor-opacity = 0.8

# --- Mouse ---
mouse-hide-while-typing = true
copy-on-select = clipboard

# --- Quick Terminal ---
quick-terminal-position = top
quick-terminal-screen = mouse
quick-terminal-autohide = true
quick-terminal-animation-duration = 0.15

# --- Security ---
clipboard-paste-protection = true
clipboard-paste-bracketed-safe = true

# --- Shell Integration ---
shell-integration = zsh

# --- Claude 专属优化 ---
# initial-command = /opt/homebrew/bin/claude   # 装好claude-code后再取消注释
initial-window = true
quit-after-last-window-closed = true
notify-on-command-finish = always

# --- Performance ---
scrollback-limit = 25000000

# --- 基础分屏（左右添加屏幕）---
keybind = cmd+d=new_split:right
keybind = cmd+shift+enter=toggle_split_zoom
keybind = cmd+shift+f=toggle_split_zoom
```

## 使用方法

1. 安装 [Ghostty](https://github.com/ghostty-org/ghostty)
2. 将配置文件复制到 `~/.config/ghostty/config`
3. 重启 Ghostty 或按 `Cmd + Shift + ,` 重载配置
