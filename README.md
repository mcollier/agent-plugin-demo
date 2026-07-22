# Agent Plugin Demo

A shared hub for engineers to discover, share, and contribute **AI agent coding plugins**. Extend **GitHub Copilot** and **Claude Code** with specialized capabilities built and refined by me!

[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![GitHub Repository](https://img.shields.io/badge/Repository-GitHub-black?style=flat-square&logo=github)](https://github.com/mcollier/agent-plugin-demo)
[![MegaLinter](https://github.com/mcollier/agent-plugin-demo/actions/workflows/mega-linter.yml/badge.svg)](https://github.com/mcollier/agent-plugin-demo/actions/workflows/mega-linter.yml)

[Overview](#overview) • [Browse Plugins](#browse-available-plugins) • [Quick Start](#quick-start)

## Overview

The Marketplace is a curated collection of **reusable, vetted plugins** built by and for our engineering team. Instead of building the same capabilities repeatedly across projects, this marketplace enables us to share proven solutions and collaborate on extending AI agent coding tools.

Each plugin in the marketplace can include any combination of:

- **Skills** - Composable capabilities that Claude/Copilot automatically invoke based on context
- **Agents** - Specialized autonomous agents tailored to our projects and workflows  
- **Hooks** - Event handlers that integrate with our development processes
- **MCP Servers** - Integrations with our tools and services (databases, APIs, internal systems)

:bulb: **Plugins can bundle external components too**: Skills, agents, and MCP servers can come from public sources and vendors (Microsoft, Anthropic, GitHub, Figma, etc.). This marketplace helps us curate, package, and share those integrations alongside our own innovations.

## Why This Matters

A shared plugin marketplace accelerates engineering work by building on collective knowledge and reducing duplication:

### :dart: Discover in One Place

Stop searching across Teams, email, and scattered repos. Find vetted, reusable plugins for common engineering tasks.

### :handshake: Collaborate and Build Together

Share your best tools with the team. When you create a useful agent or skill, other engineers can adopt and build on it. This creates a positive feedback loop where the marketplace becomes more valuable as we contribute more.

### :zap: Ship Faster

Reuse proven plugins instead of reinventing solutions. This means quicker onboarding to new projects, consistency across codebases, and less context-switching as you move between projects.

### :package: Standardize Our Tooling

A centralized marketplace means we all have access to the same high-quality, vetted tools. This ensures consistency across projects, makes team knowledge transferable, and lets us establish best practices together.

### :office: Internal-First Approach

This marketplace is built for our team's needs. Plugins can integrate with our tools, follow our standards, and reflect our engineering practices.

## Browse Available Plugins

### Current Plugins

#### Demo Plugin

A demonstration plugin showcasing the capabilities of the marketplace.

- **Description**: A demo plugin
- **Version**: 1.0.0
- **Contents**: Sample agents, skills, and MCP server configurations
- **Location**: [`plugins/demo`](plugins/demo)

> :bulb: **Looking for more plugins?** Check the [plugins directory](plugins) to browse all available contributions. Each plugin includes a `plugin.json` with details and links to documentation.

## Quick Start

### Adding to GitHub Copilot CLI

``` shell
/plugin marketplace add mcollier/agent-plugin-demo
```

### Adding to Claude Code

``` shell
/plugin marketplace add mcollier/agent-plugin-demo
```

### Visual Studio Code

Please refer to the Visual Studio Code documentation on [configuring plugin marketplaces](https://code.visualstudio.com/docs/agent-customization/agent-plugins#_configure-plugin-marketplaces).


Once you've added the `mcollier/agent-plugin-demo`, search/filter for `@agentPlugins` in the Visual Studio Code extensions. This will show you all plugins available from the built-in and configured marketplaces.  Search for `mcollier` to narrow the results.

## Resources

- :book: [Demo Plugin](plugins/demo) - An example plugin to use as a reference  
- :link: [GitHub Copilot Plugin Docs](https://docs.github.com/en/copilot/concepts/agents/about-plugins) - Official docs
- :link: [Claude Code Plugin Docs](https://code.claude.com/docs/en/plugins) - Official docs
- :link: [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - MCP specification
