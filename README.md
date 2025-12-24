# ✨ SherAtrium’s tmux

A **clean, Neovim-first tmux configuration** designed for macOS (iTerm2), focused on
**sessions, windows, and panes** — not editing.

This setup intentionally avoids over-configuration and keeps tmux predictable,
fast, and conflict-free when used alongside Neovim.

---

## 📚 Documentation

- 👉 **[Keybindings / Keymaps](./KEYMAPS.md)**

---

## 🧠 Philosophy

- **tmux = layout & multiplexing**
- **Neovim = editing & navigation**
- Prefix-driven (`Ctrl-a`)
- Minimal overrides
- Zero keybinding conflicts
- No session persistence (ephemeral workspaces)
- Works perfectly with `vim-tmux-navigator`

tmux is treated as a **live workspace manager**, not a stateful recovery tool.

---

## 🧩 Features

- `Ctrl-a` prefix (macOS-safe, ergonomic)
- Splits open in the **current working directory**
- Seamless pane navigation via `vim-tmux-navigator`
- Vim-style copy mode
- Clean, themed statusline
- Fish shell as default inside tmux
- No session autosave / restore (intentional)
