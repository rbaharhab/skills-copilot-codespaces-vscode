# Enabling Copilot Agent Dropdown in VS Code

This guide explains how to enable the Copilot agent dropdown list in your local VS Code IDE to include Claude, Copilot, and Codex.

## Overview

The agent dropdown feature allows you to switch between different AI coding assistants (Claude, GitHub Copilot, and Codex) directly from your VS Code interface, giving you flexibility in choosing the right AI tool for your task.

## Prerequisites

1. **VS Code** (version 1.85 or later recommended)
2. **GitHub Copilot subscription** (Individual, Business, or Enterprise)
3. **GitHub Copilot extensions** installed:
   - GitHub.copilot
   - GitHub.copilot-chat

## Setup Steps

### Step 1: Configure VS Code Settings

The repository includes a `.vscode/settings.json` file with the necessary configuration. These settings will:

- Enable the agent selector feature
- Enable the chat agent dropdown
- Configure available AI agent providers (Copilot, Claude, Codex)

**Key settings:**
```json
{
    "github.copilot.advanced": {
        "agentSelector": {
            "enabled": true
        }
    },
    "github.copilot.chat.agentDropdown.enabled": true,
    "github.copilot.chat.agentProviders": [
        "copilot",
        "claude",
        "codex"
    ]
}
```

### Step 2: Use GitHub Codespaces (Recommended)

The easiest way to use this configuration is through GitHub Codespaces:

1. Fork or clone this repository
2. Click the **Code** button → **Codespaces** → **Create codespace on branch**
3. Wait for the codespace to initialize
4. The `.devcontainer/devcontainer.json` will automatically:
   - Install GitHub Copilot extensions
   - Apply the agent dropdown settings

### Step 3: Set Up Local VS Code

If you prefer to work locally:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rbaharhab/skills-copilot-codespaces-vscode.git
   cd skills-copilot-codespaces-vscode
   ```

2. **Open in VS Code:**
   ```bash
   code .
   ```

3. **Install required extensions:**
   - Open the Extensions view (Ctrl/Cmd+Shift+X)
   - Search for and install:
     - `GitHub.copilot`
     - `GitHub.copilot-chat`

4. **Reload VS Code** to apply settings from `.vscode/settings.json`

### Step 4: Authenticate GitHub Copilot

1. Click on the GitHub Copilot icon in the status bar (bottom right)
2. Sign in with your GitHub account that has Copilot access
3. Authorize the Copilot extension

### Step 5: Access the Agent Dropdown

Once configured, you can access the agent dropdown:

1. **Via Chat Panel:**
   - Open Copilot Chat (Ctrl/Cmd+Shift+I or click the chat icon)
   - Look for the agent selector dropdown at the top of the chat panel
   - Click the dropdown to select between Claude, Copilot, or Codex

2. **Via Inline Chat:**
   - Press Ctrl/Cmd+I while editing a file
   - The agent selector should appear in the inline chat interface

3. **Via Command Palette:**
   - Press Ctrl/Cmd+Shift+P
   - Type "Copilot: Select Agent"
   - Choose your preferred agent

## Agent Descriptions

### GitHub Copilot
- **Best for:** General code completion and suggestions
- **Strengths:** Fast inline suggestions, trained on public GitHub code
- **Use cases:** Autocomplete, function generation, boilerplate code

### Claude (Anthropic)
- **Best for:** Complex reasoning and detailed explanations
- **Strengths:** Long-context understanding, careful analysis, safety-focused
- **Use cases:** Code review, debugging, architecture discussions

### Codex (OpenAI)
- **Best for:** Natural language to code translation
- **Strengths:** Understanding conversational requests, multi-language support
- **Use cases:** Converting descriptions to code, quick prototypes

## Verification

To verify the agent dropdown is working:

1. Open a code file (e.g., create `test.js`)
2. Open Copilot Chat (Ctrl/Cmd+Shift+I)
3. Look for a dropdown menu near the top of the chat panel
4. You should see options for "Copilot", "Claude", and "Codex"

## Troubleshooting

### Agent Dropdown Not Appearing

If you don't see the agent dropdown:

1. **Check VS Code version:**
   - Ensure you're running VS Code 1.85 or later
   - Update to the latest version if needed

2. **Verify extension versions:**
   - Update GitHub Copilot extensions to the latest version
   - Check for insider/preview builds if the feature is experimental

3. **Check Copilot subscription:**
   - Ensure your GitHub account has active Copilot access
   - Business/Enterprise plans may have additional agent access

4. **Review settings:**
   - Open Settings (Ctrl/Cmd+,)
   - Search for "copilot agent"
   - Verify `github.copilot.chat.agentDropdown.enabled` is set to `true`

5. **Reload VS Code:**
   ```
   Developer: Reload Window
   ```

### Agent Not Available

If a specific agent (Claude or Codex) isn't available:

- **Access requirements:** Claude and Codex integration may require:
  - GitHub Copilot Business or Enterprise subscription
  - Specific API access or beta enrollment
  - Additional authentication steps

- **Alternative approach:** Some organizations need to enable multi-model access through GitHub Enterprise settings

### Configuration Not Applying

If settings aren't taking effect:

1. Check for conflicting user/workspace settings
2. Ensure `.vscode/settings.json` is in the repository root
3. Restart VS Code completely (not just reload)
4. Check the Output panel (View → Output → GitHub Copilot) for errors

## Advanced Configuration

### User-Level Settings

To apply these settings globally (all projects), add to your user settings:

1. Open Settings (Ctrl/Cmd+,)
2. Click the "Open Settings (JSON)" icon in the top right
3. Add the agent configuration from `.vscode/settings.json`

### Workspace-Specific Settings

The included `.vscode/settings.json` provides workspace-specific settings that only apply to this project.

### Devcontainer Settings

The `.devcontainer/devcontainer.json` automatically configures Codespaces and Dev Containers with:
- Required extensions
- Agent dropdown enablement
- Optimal defaults for the development environment

## Additional Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [VS Code Settings Reference](https://code.visualstudio.com/docs/getstarted/settings)
- [Copilot Chat Documentation](https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-your-ide)
- [GitHub Codespaces Documentation](https://docs.github.com/en/codespaces)

## Notes

- **Feature Availability:** The agent dropdown feature may be in preview/beta. Availability of Claude and Codex depends on your GitHub Copilot subscription tier and organization settings.

- **Privacy:** Each AI agent may have different data handling and privacy policies. Review your organization's policies before using different agents.

- **Performance:** Different agents may have varying response times and capabilities depending on the task.

## Support

If you encounter issues:

1. Check the [GitHub Copilot Discussion Board](https://github.com/orgs/community/discussions/categories/copilot)
2. Review [GitHub Status](https://www.githubstatus.com/) for service issues
3. Contact your organization's GitHub administrator for enterprise configurations

---

**License:** MIT License
**Last Updated:** March 2026
