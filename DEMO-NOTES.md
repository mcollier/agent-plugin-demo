---
marp: true
---
# CONDG - July 23, 2026

## The Challenge

What are agentic tools are other engineers at my computing using?
- custom agents
- custom skills
- collection of MCP servers
- a few hooks

:tada: Innovating on solutions to make agentic software engineering more efficient.

:cry: Not sharing. If they did, it was an email or Teams message.

**Needed a better way.**  Create a web site?  A Teams channel?  A GitHub repo?

---

## Marketplace

Noticed that many vendors were sharing their agents & skills via a marketplace, with specific plugins.

### What?

The Marketplace is a curated collection of plugins.

Copilot comes with two marketplaces already registered by default: **copilot-plugins** and **awesome-copilot**.

---

## Plugin

:electric_plug: Each plugin can include any combination of:

- **Skills**: Composable capabilities that Claude/Copilot automatically invoke based on context
- **Agents**: Specialized autonomous agents tailored to our projects and workflows
- **Hooks**: Event handlers that integrate with our development processes
- **MCP Servers**: Integrations with our tools and services (databases, APIs, internal systems)

:bulb: Plugin marketplaces supported by GitHub Copilot, Claude Code, VS Code, Claude Desktop, ChatGPT, Codex, etc.

---

## marketplace.json
 Claude Code and GitHub Copilot look in the `.claude-plugin\marketplace.json` file.

```json
{
    "name": "agent-marketplace-demo",
    "owner": {
        "name": "Michael S. Collier",
        "email": "no-reply@email.com"
    },
    "plugins": [
        {
            "name": "demo-plugin",
            "description": "A demo plugin for the people.",
            "version": "1.0.0",
            "source": "./plugins/demo"
        }
    ]
}
```

---

## plugin.json

Goes in your plugin directory - `plugins/demo/plugin.json`
```json
{
    "name": "demo-plugin",
    "description": "A wonderful demo plugin.",
    "version": "1.0.0",
    "author":{
        "name": "Michael S. Collier"
    },
    "homepage": "https://www.michaelscollier.com",
    "repository": "https://github.com/mcollier/agent-plugin-demo",
    "license": "MIT",
    "mcpServers": "./.mcp.json"
}
```

---

## Creating and testing locally

### Adding to GitHub Copilot CLI

``` shell
/plugin marketplace add mcollier/agent-plugin-demo
```

### Adding to Claude Code

``` shell
/plugin marketplace add mcollier/agent-plugin-demo
```

### VS Code

Once you've added the `mcollier/agent-plugin-demo`, search/filter for `@agentPlugins` in the Visual Studio Code extensions. This will show you all plugins available from the built-in and configured marketplaces.  Search for `mcollier` to narrow the results.

---

## Publishing on GitHub

---

## Require marketplace and plugins in your repo

Define in `.github/copilot/settings` or `.claude/settings.json`

```json
{
  "extraKnownMarketplaces": {
    "company-tools": {
      "source": {
        "source": "github",
        "repo": "mcollier/agent-plugin-demo"
      }
    }
  },
  "enabledPlugins": {
    "demo-plugin@agent-marketplace-demo": true
  }
}

```

---

## Always available marketplace and plugin

VS Code