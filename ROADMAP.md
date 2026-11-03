# Lara Roadmap

Lara is a VS Code fork targeting developers who want a minimal, keyboard-driven editor with LazyVim-style UX and powerful enterprise debugging — no bloat, no telemetry, no Copilot.

---

## Phase 0 — Foundation ✅
> Goal: working VS Code fork that builds cleanly

- [x] Shallow-clone microsoft/vscode (`main`, v1.142.0)
- [x] Add `upstream` remote for future merges
- [x] Move repo to path without spaces to fix native module compilation
- [ ] `npm ci` completes without errors
- [ ] `./scripts/code.sh` launches stock VS Code

---

## Phase 1 — Rebrand
> Goal: it says Lara, not Visual Studio Code

- [ ] `product.json` — rename app, data folders, window title, URLs
- [ ] Replace VS Code icon set with Lara branding
- [ ] Switch extension gallery from VS Marketplace → Open VSX Registry
- [ ] Strip telemetry, crash reporting, and all Codex/Copilot/Chat extensions
- [ ] Remove Microsoft-specific auth and account UI

---

## Phase 2 — LazyVim UI
> Goal: keyboard-first, distraction-free interface

- [ ] **Dashboard** — startup screen with recent projects, keybind cheat sheet
- [ ] **Leader-key palette** — `<Space>` opens a Which-Key-style command menu
- [ ] **Minimal statusline** — mode indicator, file, branch, LSP status only
- [ ] Remove Activity Bar by default (toggle with `<leader>e`)
- [ ] Collapsible sidebar that doesn't steal focus
- [ ] Smooth buffer/tab switching (Harpoon-style marks)
- [ ] `<leader>ff` fuzzy file find, `<leader>fg` live grep (Telescope-style)

---

## Phase 3 — Enterprise Debugging
> Goal: best-in-class debugging UX built on DAP

- [ ] **Multi-session debugger** — attach to several processes simultaneously, each in its own pane
- [ ] **Inline variable lens** — values shown inline in the editor (not just hover)
- [ ] **Time-travel stepping** — rr/LLDB time-travel integration where available
- [ ] **Flamegraph view** — CPU profile visualization inside the editor
- [ ] **Log point templates** — snippet-based logpoints with structured output
- [ ] **Condition builder UI** — visual breakpoint conditions (no manual expression typing)
- [ ] Docker / Kubernetes attach workflows built into the debug picker

---

## Phase 4 — Distribution
> Goal: users can install and update Lara

- [ ] Code-sign macOS `.app` bundle
- [ ] GitHub Releases CI pipeline (tag → build → upload)
- [ ] Auto-update mechanism (Squirrel or custom)
- [ ] Windows NSIS/MSI installer
- [ ] Linux `.deb` / `.rpm` / AppImage
- [ ] Lara website + docs

---

## Upstream sync policy

Lara tracks `microsoft/vscode` `main`. Merge cadence: monthly, or on security patches. Lara-specific commits are prefixed `[lara]` to keep rebases clean.
