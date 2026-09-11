# Global directives

[Global-Directives.md](Global-Directives.md) is the common instruction source for Codex and Claude Code. Install identical content for both tools; maintain changes in the common source.

## Installation

Review and back up existing instructions before replacement. Preserve required project guidance in project instruction files and host setup details in local configuration.

Copy `Global-Directives.md` to the applicable user instruction location:

| Tool | Destination |
| --- | --- |
| Codex | `AGENTS.md` inside the configured Codex home directory; the default is `~/.codex`, overridden by `CODEX_HOME`. |
| Claude Code | The user-level `CLAUDE.md`; the default location is `~/.claude/CLAUDE.md`. |

The `~` notation means the current account's home directory; resolve paths using the host shell and active tool configuration. Consult the official [Codex instruction discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md) and [Claude Code instruction locations](https://code.claude.com/docs/en/memory#choose-where-to-put-claude-md-files) for custom setups.

Confirm both installed files match the common source. Start fresh sessions and inspect the active instruction sources. An active Codex `AGENTS.override.md` takes precedence over `AGENTS.md` at the same scope. [Codex discovery rules](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

## Optional enforcement

The package contains directives and installation guidance. Safety hooks, deletion helpers, and configuration skills require separate installation and validation for the selected tool and host. Loading instruction files does not install hooks or establish enforcement. [Claude Code guidance and enforcement](https://code.claude.com/docs/en/memory#claude-md-vs-auto-memory)

Recursive deletion requires a configured mechanism verified to send targets to Recycle Bin or Trash. Without that capability, stop recursive deletion and report the missing capability. The deletion restrictions and auto-memory ban still apply without installed hooks.

Keep local helper paths and hook bindings in host configuration. Keep project-specific review workflows and transmission consent in project guidance; the global consent rule preserves existing authorization without granting new transmission permission.
