# 📄 tmux Keymaps Overview

This document describes the **tmux keybindings** used in this setup.

The configuration is designed to work **alongside Neovim**, not replace it.  
tmux handles **sessions, windows, and panes**, while **Neovim handles editing and navigation inside files**.

---

## 🧠 Philosophy

- Prefix-driven (`Ctrl-a`)
- Neovim-first workflow
- Zero keybinding conflicts
- Minimal overrides
- Defaults are kept **only if they are useful**

---

## 🔑 Prefix

| Key             | Description                          |
| --------------- | ------------------------------------ |
| `Ctrl-a`        | tmux leader / prefix                 |
| `Ctrl-a Ctrl-a` | Send literal `Ctrl-a` to application |

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

## 🔀 Pane Movement (Reordering)

| Key          | Action                           |
| ------------ | -------------------------------- |
| `prefix + {` | Move pane left _(default tmux)_  |
| `prefix + }` | Move pane right _(default tmux)_ |

> Useful for rearranging layouts without recreating panes.

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

> Copy mode uses **vim-style keys** (`mode-keys vi`).

---

## 🗂 Sessions

| Key          | Action               |
| ------------ | -------------------- |
| `prefix + s` | Session picker       |
| `prefix + d` | Detach from session  |
| `prefix + X` | Kill current session |

---

## 🔌 Plugins (tmux)

| Key                | Action                                  |
| ------------------ | --------------------------------------- |
| `prefix + I`       | Install plugins (TPM) _(default)_       |
| `prefix + U`       | Update plugins (TPM) _(default)_        |
| `prefix + Alt + u` | Remove unused plugins (TPM) _(default)_ |

---

## 🔧 Utilities

| Key          | Action                           |
| ------------ | -------------------------------- |
| `prefix + r` | Reload tmux config               |
| `prefix + :` | tmux command prompt _(default)_  |
| `prefix + ?` | Show all keybindings _(default)_ |

---

## 🧩 Defaults Intentionally Kept

The following default tmux behaviors are **kept intentionally**:

- Window number selection: `prefix + 0–9`
- Copy mode entry: `prefix + [`
- Paste buffer: `prefix + ]`
- Pane reordering: `prefix + {` / `prefix + }`
- Rename window: `prefix + $`
- Focus next window: `prefix + o`
- Help & command prompt
