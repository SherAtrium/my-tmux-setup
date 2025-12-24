# 📄 tmux Keymaps Overview

This document describes the **tmux keybindings** used in this setup.

The configuration is designed to work **alongside Neovim**.
tmux handles **sessions, windows, panes, and layout**, while **Neovim handles editing and navigation inside files**.

---

## 🧠 Philosophy

- Prefix-driven (`Ctrl-a`)
- Neovim-first workflow
- Zero keybinding conflicts
- Minimal overrides
- Defaults are kept **only when useful**
- tmux sessions are **ephemeral** (no auto save / restore)

---

## 🔑 Prefix

| Key      | Description          |
| -------- | -------------------- |
| `Ctrl-a` | tmux leader / prefix |

> Default `Ctrl-b` is unbound.

---

## 🪟 Windows (tmux = Tabs)

| Key            | Action                                    |
| -------------- | ----------------------------------------- |
| `prefix + c`   | New window (opens in current directory)   |
| `prefix + ,`   | Rename current window                     |
| `prefix + x`   | Close current window                      |
| `prefix + n`   | Next window                               |
| `prefix + p`   | Previous window                           |
| `prefix + w`   | Window picker (tree view)                 |
| `prefix + o`   | Focus next window _(default tmux)_        |
| `prefix + $`   | Rename window _(default tmux)_            |
| `prefix + 0–9` | Jump to window by number _(default tmux)_ |

---

## 🧩 Panes (Splits)

| Key           | Action                               |
| ------------- | ------------------------------------ |
| `prefix + \|` | Vertical split (current directory)   |
| `prefix + -`  | Horizontal split (current directory) |
| `prefix + q`  | Close current pane                   |
| `prefix + z`  | Zoom / unzoom pane                   |

---

## 🔀 Pane Reordering (Defaults)

| Key          | Action          |
| ------------ | --------------- |
| `prefix + {` | Move pane left  |
| `prefix + }` | Move pane right |

---

## 🧭 Pane Navigation

Pane navigation is handled by **vim-tmux-navigator**.

| Context        | Key                                   |
| -------------- | ------------------------------------- |
| Inside Neovim  | `<C-h>` / `<C-j>` / `<C-k>` / `<C-l>` |
| Outside Neovim | `prefix + h` / `j` / `k` / `l`        |

> tmux itself does not define pane-navigation bindings.

---

## 📏 Pane Resizing

| Key          | Action            |
| ------------ | ----------------- |
| `prefix + h` | Resize pane left  |
| `prefix + j` | Resize pane down  |
| `prefix + k` | Resize pane up    |
| `prefix + l` | Resize pane right |

> Resizing is repeatable while holding the key.

---

## 📋 Copy Mode (Vim-style)

| Key          | Action                           |
| ------------ | -------------------------------- |
| `prefix + [` | Enter copy mode _(default tmux)_ |
| `v`          | Begin selection                  |
| `y`          | Yank selection and exit          |
| `q`          | Exit copy mode _(default tmux)_  |

---

## 🗂 Sessions

| Key          | Action               |
| ------------ | -------------------- |
| `prefix + s` | Session picker       |
| `prefix + d` | Detach from session  |
| `prefix + X` | Kill current session |

> Session persistence is intentionally **disabled**.

---

## 🔌 Plugin Management (TPM)

| Key                | Action                |
| ------------------ | --------------------- |
| `prefix + I`       | Install plugins       |
| `prefix + U`       | Update plugins        |
| `prefix + Alt + u` | Remove unused plugins |

---

## 🔧 Utilities

| Key          | Action                           |
| ------------ | -------------------------------- |
| `prefix + r` | Reload tmux config               |
| `prefix + :` | tmux command prompt _(default)_  |
| `prefix + ?` | Show all keybindings _(default)_ |

---

## 📂 Working Directory Behavior

- New panes and windows always open in the **current pane directory**
- Avoids falling back to `$HOME`
- Designed for project-based workflows

---

## 🐚 Shell

- tmux always starts with **fish** as the default shell
- Statusline shows the active command or shell (e.g. `fish`, `zsh`, `nvim`)
