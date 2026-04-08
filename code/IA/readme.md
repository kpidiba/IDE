# AI Coding Assistants in VS Code: GitHub Copilot, Windsurf & Roo Code

A practical guide to the most popular AI-powered coding tools you can use inside **Visual Studio Code** (or VS Code forks).

## Overview

Modern development in VS Code is supercharged by AI. Here’s a quick comparison of three leading options:

| Tool               | Type                                                 | Pricing                                                | Best For                                                 | Key Strength                     | Bring Your Own Key (BYOK)    |
| ------------------ | ---------------------------------------------------- | ------------------------------------------------------ | -------------------------------------------------------- | -------------------------------- | ---------------------------- |
| **GitHub Copilot** | Official Microsoft extension                         | $10/mo (Individual)<br>$19–39/mo (Business/Enterprise) | Everyday coding, inline suggestions, enterprise teams    | Seamless **autocomplete** & chat | Limited (uses GitHub models) |
| **Windsurf**       | AI-native IDE + VS Code extension (formerly Codeium) | Free tier + ~$15/mo Pro                                | Fast prototyping, agentic workflows, flow state          | **Cascade** agent & low latency  | Partial                      |
| **Roo Code**       | Open-source VS Code extension                        | **Completely Free** (pay only for your LLM API usage)  | Custom workflows, full control, multi-file agentic tasks | **Custom Modes** & orchestration | Full BYOK support            |

### 1. GitHub Copilot — The Classic Inline Assistant

**GitHub Copilot** is the most widely used AI coding tool. It lives directly inside VS Code and provides:

- Real-time **inline code completions** (just keep typing — hit Tab to accept)
- **Copilot Chat** sidebar for asking questions, explaining code, refactoring, and generating tests
- Multi-file editing via **Copilot Agent** / Workspace (newer versions)
- Excellent integration with GitHub, Microsoft ecosystem, and enterprise security features

**When to choose Copilot:**

- You want frictionless autocomplete that feels like magic
- You work in large teams with compliance requirements
- You prefer a polished, "just works" experience without managing API keys

**Installation:**

1. Install the **GitHub Copilot** and **GitHub Copilot Chat** extensions from the VS Code Marketplace.
2. Sign in with your GitHub account and activate your subscription.

### 2. Windsurf — The AI-Native Coding Experience

**Windsurf** (rebranded and evolved from Codeium) offers both a full **Windsurf Editor** (a VS Code fork) and a powerful **Windsurf Plugin** for regular VS Code.

Key features:

- Lightning-fast autocomplete and chat
- **Cascade** — an autonomous agent that can handle complex, multi-step tasks
- Deep codebase understanding and natural language editing
- Excellent for staying "in flow" with minimal context switching

Many developers find Windsurf’s chat and agent capabilities more polished and responsive than standard Copilot.

**When to choose Windsurf:**

- You want a more **agentic** experience (the AI does more heavy lifting)
- You prototype quickly or work on new projects
- You like the familiarity of VS Code but with stronger AI integration

**Installation in VS Code:**
Search for **"Windsurf Plugin"** (formerly Codeium) in the Extensions view.

### 3. Roo Code — The Open-Source AI Dev Team

**Roo Code** (also called RooCode) is a free, open-source VS Code extension that turns your editor into a full AI-powered development team.

Standout features:

- **Multiple Modes**: Code, Architect, Ask, Debug, and fully **Custom Modes**
- Multi-file reading, writing, refactoring, and command execution
- Complete control — **Bring Your Own Key** (OpenAI, Anthropic/Claude, Gemini, local models, OpenRouter, etc.)
- Transparent cost tracking
- Highly customizable rules, skills, and workflows

It excels at complex, orchestrated tasks where you need the AI to plan, execute, and iterate across your entire project.

**When to choose Roo Code:**

- You want **maximum flexibility** and control over models and costs
- You love customizing your AI workflow
- You prefer open-source tools and don’t want to pay a monthly subscription fee (only LLM usage)

**Installation:**

1. Open VS Code → Extensions (Ctrl+Shift+X)
2. Search for **"Roo Code"**
3. Install and add your API keys in the settings
4. Open the Roo panel via the kangaroo icon in the sidebar

## Quick Recommendation

- **Just starting out or want simplicity** → **GitHub Copilot**
- **Maximum speed + agentic power in a clean IDE feel** → **Windsurf**
- **Full control, customization, and no subscription** → **Roo Code**

Many power users run **two or even all three** together:

- Copilot or Windsurf for fast inline completions
- Roo Code for deep multi-file agent work

## Tips for Best Results

- Use **good prompts** — be specific about language, framework, and style
- Combine tools: Let autocomplete handle small parts, and agent/chat handle architecture/refactoring
- Review AI-generated code carefully (especially in complex projects)
- Experiment with different models in Roo Code to find what works best for your stack

## Resources

- [GitHub Copilot Docs](https://docs.github.com/en/copilot)
- [Windsurf](https://windsurf.com/)
- [Roo Code](https://roocode.com/) + [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=RooVeterinaryInc.roo-cline)

---

Happy coding! 🚀

Feel free to contribute tips, examples, or updates to this guide.
