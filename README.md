# Lara

A minimal, keyboard-first code editor, forked from [Visual Studio Code](https://github.com/microsoft/vscode) (`Code - OSS`).

Lara aims to feel like [LazyVim](https://www.lazyvim.org/) inside a full graphical editor: a leader-key command menu, a quiet statusline, fuzzy find and live grep on the keyboard, and a serious debugger. It ships without telemetry, crash reporting or Copilot/Chat.

> **Status: early.** Right now this is a clean VS Code fork that builds. The rebrand and UI work described in [ROADMAP.md](ROADMAP.md) have not started, so what you run today is stock Code - OSS.

## Goals

- **Rebrand.** Lara name, icons and data folders, with extensions from [Open VSX](https://open-vsx.org/) instead of the Microsoft Marketplace.
- **No bloat.** Telemetry, crash reporting, Microsoft account UI and built-in AI features removed.
- **LazyVim-style UI.** `<Space>` leader menu, minimal statusline, a dashboard, hidden activity bar, `<leader>ff` and `<leader>fg`.
- **Better debugging.** Multi-session debugging, inline variable values, flamegraphs, a visual breakpoint-condition builder, and Docker/Kubernetes attach.

See [ROADMAP.md](ROADMAP.md) for the phased plan.

## Build from source

Lara builds the same way as VS Code. You need Node.js (see `.nvmrc`), Python, and the native build tools for your platform. **Clone to a path without spaces**, or native module compilation fails.

```bash
git clone https://github.com/ker0s3ner/Lara.git
cd Lara
npm ci
./scripts/code.sh        # scripts\code.bat on Windows
```

The full toolchain requirements are in the upstream [How to Contribute](https://github.com/microsoft/vscode/wiki/How-to-Contribute) guide.

## Staying in sync with upstream

```bash
git remote add upstream https://github.com/microsoft/vscode.git
git fetch upstream
git merge upstream/main
```

## License

Lara inherits the [MIT license](LICENSE.txt) of Code - OSS. "Visual Studio Code" and its logos are Microsoft trademarks, and Lara is not affiliated with or endorsed by Microsoft.
