# Quick Setup Guide: Enable Copilot Agent Dropdown

## For Codespaces (Easiest Method)

1. Fork or open this repository in GitHub
2. Click **Code** → **Codespaces** → **Create codespace**
3. Wait for initialization - agent dropdown will be automatically configured!
4. Open Copilot Chat (Ctrl/Cmd+Shift+I) and look for the agent selector

## For Local VS Code

### Quick Steps:

1. **Clone and open repository:**
   ```bash
   git clone https://github.com/rbaharhab/skills-copilot-codespaces-vscode.git
   cd skills-copilot-codespaces-vscode
   code .
   ```

2. **Install extensions** (if not already installed):
   - `GitHub.copilot`
   - `GitHub.copilot-chat`

3. **Reload VS Code** - Settings are already configured in `.vscode/settings.json`

4. **Sign in to GitHub Copilot** via the status bar

5. **Access agent dropdown:**
   - Open Copilot Chat (Ctrl/Cmd+Shift+I)
   - Look for agent selector dropdown at top
   - Select between Copilot, Claude, or Codex

## What's Configured

### `.vscode/settings.json`
- Enables agent selector feature
- Configures Copilot, Claude, and Codex as available agents
- Enables inline suggestions

### `.devcontainer/devcontainer.json`
- Auto-installs Copilot extensions in Codespaces
- Pre-configures agent dropdown settings

## Troubleshooting

**No dropdown visible?**
- Update VS Code to version 1.85+
- Update Copilot extensions to latest version
- Reload VS Code window
- Check your Copilot subscription tier (Business/Enterprise may be needed for multi-agent support)

**Agent not available?**
- Claude and Codex may require GitHub Copilot Business/Enterprise
- Contact your organization's GitHub admin for access

## Full Documentation

See **[AGENT_DROPDOWN_SETUP.md](./AGENT_DROPDOWN_SETUP.md)** for complete setup instructions, troubleshooting, and advanced configuration.

## Key Settings

```json
{
    "github.copilot.advanced": {
        "agentSelector": {"enabled": true}
    },
    "github.copilot.chat.agentDropdown.enabled": true,
    "github.copilot.chat.agentProviders": ["copilot", "claude", "codex"]
}
```

---

**Questions?** See the [full documentation](./AGENT_DROPDOWN_SETUP.md) or [GitHub Copilot Docs](https://docs.github.com/en/copilot).
