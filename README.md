# <picture><source media="(prefers-color-scheme: dark)" srcset="docs/leverage-dark.svg"><img src="docs/leverage-light.svg" alt="Leverage Computer" height="24"></picture> Codex on Leverage

<a href="https://leverage.computer/integrations/#codex"><img src="https://img.shields.io/badge/Docs-leverage.computer-3f3f46?labelColor=0a0a0a" alt="Docs on leverage.computer"></a>
<a href="#features"><img src="https://img.shields.io/badge/Connects%20over-SSH-3f3f46?labelColor=0a0a0a" alt="Connects over SSH"></a>

[Features](#features) · [Desktop](#desktop) · [Terminal](#terminal) ·
[leverage.computer](https://leverage.computer)

[![Syncing a Leverage workspace into Codex from the Leverage desktop app](docs/desktop.gif)](docs/desktop.mp4)

## Features

- **Multiplayer harness**: each prompt shows who sent it, and a teammate's
  prompt appears as soon as they send it.
- **Company computer**: sessions run in Leverage's sandbox and are shared with
  your team. Leverage hosts the SSH server, `ssh.leverage.computer`, so you
  don't run one.
- **Steering**: your prompt shows at once and steers a running turn. Prompts
  sent while it is busy wait in a queue you can list, take back or send now.
- **Governance**: the agent asks you to pick an option, approve a plan, or
  allow a call: once, for the session, or always.

Spaces show as projects, sessions as threads.

## Desktop

In the Leverage desktop app, open Settings → Developer tools and click
**Sync into Codex**.

From a terminal instead:

```sh
leverage login
leverage ssh setup
leverage codex setup

# add another workspace
leverage codex setup --workspace <slug>

# after spaces change; quit Codex first
leverage codex refresh

# when you lose a device
leverage ssh forget <fingerprint>
```

## Terminal

```sh
leverage codex engineering
```

Opens the Codex CLI on the space `engineering`.

[![A terminal runs leverage codex general. The Codex CLI opens on the space, /resume finds a session, and it opens with a teammate's messages and the agent's diff](docs/terminal.gif)](docs/terminal.mp4)

## The Leverage CLI

The terminal commands need the Leverage CLI. In the Leverage app, Settings →
Developer tools → CLI gives its install command, for macOS and Linux.

A session you start from Codex is private until you share it.
