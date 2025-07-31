
# Claude Code CLI Mounts

Mounts Claude Code configuration directories and files from the host into the devcontainer, enabling seamless access to your Claude Code settings, credentials, and customizations.

## Example Usage

```json
"features": {
    "ghcr.io/anthropics/devcontainer-features/claude-code-mounts:1": {}
}
```

## Options

| Options Id | Description | Type | Default Value |
|-----|-----|-----|-----|

## Customizations

### VS Code Extensions

- `anthropic.claude-code`

## What This Feature Does

This feature automatically mounts your Claude Code configuration from your host machine into the devcontainer, providing access to:

- **Credentials** (`~/.claude/.credentials.json`) - Your authentication tokens
- **Settings** (`~/.claude/settings.json`) - Your Claude Code configuration
- **CLAUDE.md** (`~/.claude/CLAUDE.md`) - Your global project instructions
- **Agents** (`~/.claude/agents/`) - Custom agent configurations
- **Commands** (`~/.claude/commands/`) - Custom command definitions
- **Hooks** (`~/.claude/hooks/`) - Event-driven shell commands

## Requirements

This feature requires:

1. The Claude Code CLI to be installed (use the `claude-code` feature)
2. Claude Code configuration files to exist on your host machine
3. HOME variable to be set - use "Edit user environment variables" in Windows

## Recommended Configuration

Use this feature together with the main Claude Code feature:

```json
"features": {
    "ghcr.io/devcontainers/features/node:1": {},
    "ghcr.io/anthropics/devcontainer-features/claude-code:1": {},
    "ghcr.io/anthropics/devcontainer-features/claude-code-mounts:1": {}
}
```

## Benefits

- Maintain consistent Claude Code settings across all devcontainers
- No need to reconfigure credentials in each container
- Access to your custom agents, commands, and hooks
- Seamless development experience with persistent Claude Code configuration



---

_Note: This file was auto-generated from the [devcontainer-feature.json](https://github.com/anthropics/devcontainer-features/blob/main/src/claude-code/devcontainer-feature.json).  Add additional notes to a `NOTES.md`._
