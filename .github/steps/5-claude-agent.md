<!--
  <<< Author notes: Step 5 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 5: Enable Claude Agent in VS Code

_Awesome! You've mastered using comments to generate code with Copilot!_ :rocket:

Now let's enhance your AI-powered development environment by enabling Claude Agent in VS Code. Claude is Anthropic's AI assistant that can help you with code analysis, refactoring, and complex problem-solving directly in your IDE.

**Claude Agent works seamlessly alongside GitHub Copilot, giving you multiple AI assistants to choose from based on your needs.**

### :keyboard: Activity: Enable Claude Agent extension

**We recommend opening another browser tab to work through the following activities so you can keep these instructions open for reference.**

Let's add the Claude Agent extension to your development container configuration.

1. Navigate back to your **Code** tab of your repository.
2. Open the `.devcontainer/devcontainer.json` file.
3. Update the extensions array to include the Claude Agent extension:
   ```json
   {
       // Name this configuration
       "name": "Codespace for Skills!",
       "customizations": {
           "vscode": {
               "extensions": [
                   "GitHub.copilot",
                   "Anthropic.claude-code"
               ]
           }
       }
   }
   ```
4. Commit the changes to your repository.
5. Rebuild your Codespace to apply the new configuration:
   - Press `F1` or `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac) to open the Command Palette
   - Type "Codespaces: Rebuild Container" and select it
   - Wait for the container to rebuild (this may take a few minutes)

6. Verify the Claude Agent extension is installed:
   - Click the extensions sidebar tab (square icon on the left)
   - Search for "Claude" in the extensions list
   - You should see "Claude Code" by Anthropic installed

### :keyboard: Activity: Test Claude Agent

1. Open the Command Palette (`F1` or `Ctrl+Shift+P`)
2. Type "Claude" to see available Claude commands
3. You can now use Claude Agent alongside GitHub Copilot for:
   - Code explanations and analysis
   - Refactoring suggestions
   - Debugging assistance
   - Complex problem-solving

> **Note**
> Claude Agent and GitHub Copilot complement each other - use Copilot for quick code completions and Claude for deeper analysis and conversations about your code.

### :keyboard: Activity: Push code to your repository from the codespace

1. If you made any test changes, use the VS Code terminal to stage and commit:

   ```
   git add .
   git commit -m "Enable Claude Agent"
   git push
   ```

**Wait about 60 seconds then refresh your repository landing page for the next step.**
