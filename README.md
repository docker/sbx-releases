# Dash
Safe environments for agents. Built by Docker.

[![GitHub Release](https://img.shields.io/github/v/release/docker/dash-releases?color=2560ff&labelColor=e7eaef)](https://github.com/docker/dash-releases/releases/latest)

# What it does
Dash provides sandboxes with controlled access to your filesystem, network, and tools. This means your agents can work autonomously without putting your machine or data at risk.

# Details
• Docker-native isolation. Same containerization principles trusted by 20M+ developers.
• Vendor-neutral. Works with the models and tools you’re already using.

# What you get
• YOLO mode by default: agents work without asking permission
• Private Docker daemon for running test containers
• File access controls between host and sandbox
• Network access control
• Works with Claude Code, Codex, Gemini CLI, OpenCode, and more

# Install

### Homebrew

```bash
brew install docker/tap/ds
```

### WinGet
```powershell
winget install -h Docker.ds
```

# Learn more
[Docs​​​​​​​​​​​​​​​​](https://docs.docker.com/ai/sandboxes/)

# License
Proprietary — Docker Inc.
https://github.com/docker/dash-releases/blob/HEAD/LICENSE
