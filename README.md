# Docker Sandboxes

Safe environments for agents. Built by Docker.

[![GitHub Release](https://img.shields.io/github/v/release/docker/sbx-releases?color=2560ff&labelColor=e7eaef)](https://github.com/docker/sbx-releases/releases/latest)

# What it does

It provides sandboxes with controlled access to your filesystem, network, and tools. This means your agents can work autonomously without putting your machine or data at risk.

# Details

- Docker-native isolation. Same containerization principles trusted by 20M+ developers.
- Vendor-neutral. Works with the models and tools you’re already using.

# What you get

- YOLO mode by default: agents work without asking permission
- Private Docker daemon for running test containers
- File access controls between host and sandbox
- Network access control
- Works with Claude Code, Codex, Gemini CLI, OpenCode, and more

# Install

For complete prerequisites and additional setup guidance, see the
[Docker Sandboxes documentation](https://docs.docker.com/ai/sandboxes/).

### Homebrew (macOS)

```bash
brew install docker/tap/sbx
```

### WinGet (Windows)

```powershell
winget install -h Docker.sbx
```

### APT (Ubuntu)

```bash
curl -fsSL https://get.docker.com | sudo REPO_ONLY=1 sh
sudo apt-get install docker-sbx
sudo usermod -aG kvm $USER
newgrp kvm
```


## Manual install from release artifacts

Download the artifacts for your platform from the
[latest release](https://github.com/docker/sbx-releases/releases/latest).

### macOS

Download `DockerSandboxes-darwin.tar.gz` and extract:

```bash
tar -xzf DockerSandboxes-darwin.tar.gz
```

### Windows

Download [`DockerSandboxes.msi`](https://github.com/docker/sbx-releases/releases/latest/download/DockerSandboxes.msi)
and double-click to install, or use the command line:

```powershell
msiexec /i DockerSandboxes.msi /quiet
```

### Ubuntu

Download the `.deb` package from the release and install:

```bash
sudo apt install ./DockerSandboxes-linux-amd64-ubuntu2604.deb
```

### Rocky Linux 8

Download the `.rpm` package from the release and install:

```bash
sudo dnf install ./DockerSandboxes-linux-amd64-rockylinux8.rpm
```

## Release candidates

Release candidates are the builds each stable release is promoted from, so they
are the best way to try a version before it ships. They are published as
prereleases tagged `vX.Y.Z-rcN` on the
[releases page](https://github.com/docker/sbx-releases/releases), carrying the
same artifacts as a stable release.

On macOS, you can install the current release candidate via Homebrew:

```bash
brew install docker/tap/sbx@rc
```

The `sbx`, `sbx@rc`, and `sbx@nightly` casks conflict with each other, so
uninstall the one you already have before switching:

```bash
brew uninstall --cask docker/tap/sbx
brew install docker/tap/sbx@rc
```

Release candidates are not published to WinGet or to the apt/dnf repositories —
those channels carry stable releases only. On Windows and Linux, download the
artifacts from the release candidate's own page and follow the manual install
instructions above. Because a release candidate is a prerelease,
`/releases/latest` never resolves to one; use the RC tag explicitly:

```
https://github.com/docker/sbx-releases/releases/download/<RC-TAG>/DockerSandboxes.msi
```

## Nightly releases

Nightly builds from `main` are available at
[docker/sbx-releases/releases/tag/nightly](https://github.com/docker/sbx-releases/releases/tag/nightly).

On macOS, you can install the nightly build via Homebrew:

```bash
brew install docker/tap/sbx@nightly
```

For other platforms, download the artifacts from the nightly release page and
follow the manual install instructions above.

# Feedback

If you run into issues or have feedback, please
[open an issue](https://github.com/docker/sbx-releases/issues) on this repository.

# Learn more

[Docs](https://docs.docker.com/ai/sandboxes/)

# License

Proprietary — Docker Inc.
[LICENSE](https://github.com/docker/sbx-releases/blob/HEAD/LICENSE)
