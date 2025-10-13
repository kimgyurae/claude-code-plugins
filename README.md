# Claude Code Plugins

[![Version](https://img.shields.io/badge/version-3.1.0-brightgreen)](CHANGELOG.md)
[![Plugins](https://img.shields.io/badge/plugins-224-blue)](https://github.com/kimgyurae/claude-code-plugins)
[![Beta](https://img.shields.io/badge/status-beta-orange)](https://www.anthropic.com/news/claude-code-plugins)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Discord](https://img.shields.io/badge/Discord-Claude%20Developers-5865F2)](https://discord.com/invite/6PPFFzqPDZ)
[![Discussions](https://img.shields.io/github/discussions/kimgyurae/claude-code-plugins?label=discussions)](https://github.com/kimgyurae/claude-code-plugins/discussions)
[![GitHub Stars](https://img.shields.io/github/stars/kimgyurae/claude-code-plugins?style=social)](https://github.com/kimgyurae/claude-code-plugins)

**The comprehensive marketplace and learning hub for Claude Code plugins.**

> **Important**: This marketplace contains both AI instruction templates (that guide Claude's behavior) and executable MCP servers (that run as Node.js processes). See [Understanding Plugin Types](#understanding-plugin-types) below for details.

## Browse the Marketplace

**[https://kimgyurae.github.io/claude-code-plugins/](https://kimgyurae.github.io/claude-code-plugins/)**

## Quick Start

```bash
# Add this marketplace
/plugin marketplace add kimgyurae/claude-code-plugins

# Install a plugin pack
/plugin install devops-automation-pack@claude-code-plugins
```

---

## Understanding Plugin Types

This marketplace contains **two types of plugins** that work differently:

### 1. AI Instruction Plugins (Plugin Packs & Templates)
- **What they are**: Detailed markdown instructions that guide Claude's behavior
- **How they work**: Tell Claude HOW to perform tasks using its built-in capabilities
- **Examples**: DevOps pack, Security pack, AI Agency toolkit
- **No external code execution** - work entirely through Claude's interpretation

### 2. MCP Server Plugins (Executable Code)
- **What they are**: Real TypeScript/JavaScript applications
- **How they work**: Run as separate Node.js processes that Claude can communicate with
- **Examples**: project-health-auditor, conversational-api-debugger
- **Actual compiled code** - 13-26KB of executable JavaScript

Both types are **fully functional** but operate through different mechanisms. Most plugins in this marketplace are AI instruction templates designed specifically for Claude Code.

---

## 🎉 v3.1.0 - 224 PLUGINS AVAILABLE!

**The Claude Code Plugin Hub continues to grow!** Now with **224 production-ready plugins** across 14 categories, including advanced AI-powered automation.

### Plugin Packs (62 AI Instruction Templates)

> **Note**: These packs contain AI instruction templates, not traditional executable code. They enhance Claude's capabilities through detailed guidance and templates.

| Pack | Templates | Description | Type |
|------|-----------|-------------|------|
| **devops-automation-pack** | 25 | Git workflows, CI/CD guidance, Docker best practices, Kubernetes patterns | AI Instructions |
| **security-pro-pack** | 10 | OWASP auditing steps, compliance checklists, threat modeling guides | AI Instructions |
| **fullstack-starter-pack** | 15 | React patterns, API scaffolding, database schema templates | AI Instructions |
| **ai-ml-engineering-pack** | 12 | Prompt optimization, LLM integration patterns, RAG architectures | AI Instructions |

```bash
# Install any pack
/plugin install devops-automation-pack@claude-code-plugins
/plugin install security-pro-pack@claude-code-plugins
/plugin install fullstack-starter-pack@claude-code-plugins
/plugin install ai-ml-engineering-pack@claude-code-plugins
```

---

## All Plugins

### MCP Server Plugins (5 plugins with Executable Code)

> **Real Code**: These plugins contain compiled TypeScript/JavaScript that runs as separate Node.js processes.

| Plugin | Description | Tools | Code Size | Install |
|--------|-------------|-------|-----------|---------|
| **project-health-auditor** | Code health analysis: complexity + churn + tests | 4 | 13KB TS | `/plugin install project-health-auditor@claude-code-plugins` |
| **conversational-api-debugger** | Debug REST APIs with OpenAPI specs and HTTP logs | 4 | 26KB JS | `/plugin install conversational-api-debugger@claude-code-plugins` |
| **domain-memory-agent** | Knowledge base with TF-IDF semantic search | 6 | Compiled | `/plugin install domain-memory-agent@claude-code-plugins` |
| **design-to-code** | Convert Figma/screenshots to React/Svelte/Vue | 3 | Compiled | `/plugin install design-to-code@claude-code-plugins` |
| **workflow-orchestrator** | DAG-based workflow automation | 4 | Compiled | `/plugin install workflow-orchestrator@claude-code-plugins` |

[View MCP Server Documentation →](./MCP-SERVERS-STATUS.md)

### AI Agency Toolkit (6 Template Plugins)

> **Templates**: These provide workflow templates and configuration patterns for Claude to interpret.

| Plugin | Description | Type | Install |
|--------|-------------|------|---------|
| **n8n-workflow-designer** | n8n workflow JSON templates | Templates | `/plugin install n8n-workflow-designer@claude-code-plugins` |
| **make-scenario-builder** | Make.com scenario configurations | Templates | `/plugin install make-scenario-builder@claude-code-plugins` |
| **zapier-zap-builder** | Zapier automation templates | Templates | `/plugin install zapier-zap-builder@claude-code-plugins` |
| **discovery-questionnaire** | Client discovery question sets | Templates | `/plugin install discovery-questionnaire@claude-code-plugins` |
| **sow-generator** | Statement of Work templates | Templates | `/plugin install sow-generator@claude-code-plugins` |
| **roi-calculator** | ROI calculation formulas | Templates | `/plugin install roi-calculator@claude-code-plugins` |

### Production Plugins (2 plugins)

| Plugin | Description | Install |
|--------|-------------|---------|
| **git-commit-smart** | AI-powered conventional commit messages | `/plugin install git-commit-smart@claude-code-plugins` |
| **overnight-dev** | Autonomous overnight development with TDD enforcement | `/plugin install overnight-dev@claude-code-plugins` |

### Example Plugins (3 plugins)

| Plugin | Description | Install |
|--------|-------------|---------|
| **hello-world** | Simple greeting command - perfect for learning | `/plugin install hello-world@claude-code-plugins` |
| **formatter** | Auto-formats code after edits using hooks | `/plugin install formatter@claude-code-plugins` |
| **security-agent** | Expert security agent for vulnerability detection | `/plugin install security-agent@claude-code-plugins` |

---

## What Are Claude Code Plugins?

Claude Code plugins extend Claude's capabilities through two approaches:

### Plugin Components:
- **Slash Commands** - Custom shortcuts that trigger Claude actions or templates
- **Subagents** - Specialized AI instruction sets for specific domains
- **Hooks** - Automation scripts that trigger on events (file edits, tool usage)
- **MCP Servers** - External Node.js applications that provide tools to Claude

### How They Work:
- **AI Instruction Plugins**: Work by providing Claude with detailed guidance, templates, and patterns to follow (majority of plugins)
- **MCP Server Plugins**: Run actual TypeScript/JavaScript code in separate processes that Claude can call (5 plugins)

Both types are valid Claude Code plugins - they just operate through different mechanisms.

**Released**: October 2025 (Public Beta)
**Official Docs**: https://docs.claude.com/en/docs/claude-code/plugins

---

## MCP Plugin Details

### project-health-auditor

**Identify technical debt hot spots with multi-dimensional analysis**

```bash
/plugin install project-health-auditor@claude-code-plugins
/analyze /path/to/repo  # Comprehensive analysis workflow
```

**What it does**:
- Code Complexity: Cyclomatic complexity analysis with health scores
- Git Churn: Identifies frequently changing files (hot spots)
- Test Coverage: Maps source files to tests, finds gaps
- Hot Spots: Finds files with high complexity + high churn + no tests

**MCP Tools**: `list_repo_files`, `file_metrics`, `git_churn`, `map_tests`

---

### conversational-api-debugger

**Debug REST API failures using OpenAPI specs and HTTP logs**

```bash
/plugin install conversational-api-debugger@claude-code-plugins
/debug-api  # Guided debugging workflow
```

**What it does**:
- OpenAPI Parser: Load and analyze API specs (JSON/YAML)
- HAR Support: Import browser DevTools HTTP logs
- Failure Analysis: Root cause identification with severity
- cURL Generation: Create reproducible test commands

**MCP Tools**: `load_openapi`, `ingest_logs`, `explain_failure`, `make_repro`

---

### domain-memory-agent

**Knowledge base with TF-IDF semantic search (no ML dependencies)**

```bash
/plugin install domain-memory-agent@claude-code-plugins
```

**What it does**:
- Document Storage: Store documents with tags and metadata
- Semantic Search: TF-IDF based relevance ranking
- Summarization: Extractive summaries with caching
- Organization: Tag-based filtering and categorization

**MCP Tools**: `store_document`, `semantic_search`, `summarize`, `list_documents`, `get_document`, `delete_document`

**Perfect for**: RAG systems, documentation search, knowledge management

---

### design-to-code

**Convert Figma designs and screenshots into production-ready code**

```bash
/plugin install design-to-code@claude-code-plugins
```

**What it does**:
- Figma Parsing: Extract components from Figma JSON exports
- Screenshot Analysis: Analyze UI layouts from images
- Multi-Framework: Generate React, Svelte, or Vue components
- A11y Built-in: ARIA labels, semantic HTML, keyboard navigation

**MCP Tools**: `parse_figma`, `analyze_screenshot`, `generate_component`

---

### workflow-orchestrator

**DAG-based workflow automation with parallel execution**

```bash
/plugin install workflow-orchestrator@claude-code-plugins
```

**What it does**:
- DAG Execution: Directed Acyclic Graph task dependencies
- Parallel Tasks: Execute independent tasks concurrently
- Run History: Track all workflow executions
- Status Monitoring: Real-time progress tracking

**MCP Tools**: `create_workflow`, `execute_workflow`, `get_workflow`, `list_workflows`

**Perfect for**: CI/CD pipelines, data ETL, multi-stage deployments

---

## Plugin Pack Details

### DevOps Automation Pack (25 plugins)

**Complete DevOps automation suite**

**Component Breakdown**:
- 01-git-workflow: 5 commands
- 02-ci-cd: 5 commands, 1 agent
- 03-docker: 3 commands, 1 agent
- 04-kubernetes: 3 commands, 1 agent
- 05-terraform: 3 commands, 1 agent
- 06-deployment: 1 command, 1 agent

**Total**: 20 commands, 5 agents

**Features**:
- Git workflow automation and branching strategies
- CI/CD pipeline design and optimization
- Docker containerization and optimization
- Kubernetes cluster management and deployment
- Terraform infrastructure as code
- Deployment automation and monitoring

```bash
/plugin install devops-automation-pack@claude-code-plugins
```

---

### Security Pro Pack (10 plugins)

**Professional security toolkit**

**Component Breakdown**:
- 01-core-security: 1 command, 2 agents
- 02-compliance: 1 command, 1 agent
- 03-cryptography: 1 command, 1 agent
- 04-infrastructure-security: 2 commands, 1 agent

**Total**: 5 commands, 5 agents

**Features**:
- OWASP auditing and penetration testing
- HIPAA, PCI DSS, GDPR, SOC 2 compliance checking
- Cryptography audit and key management review
- Threat modeling and container scanning
- API security and infrastructure hardening

```bash
/plugin install security-pro-pack@claude-code-plugins
```

---

### Fullstack Starter Pack (15 plugins)

**Complete fullstack development toolkit**

**Component Breakdown**:
- 01-frontend: 2 commands, 2 agents
- 02-backend: 2 commands, 2 agents
- 03-database: 2 commands, 1 agent
- 04-integration: 3 commands, 1 agent

**Total**: 9 commands, 6 agents

**Features**:
- React components and UI/UX design
- Express/FastAPI scaffolding and API patterns
- PostgreSQL schemas and Prisma ORM
- Authentication setup and environment config
- Full project scaffolding and deployment

**Perfect for**: Bootcamp grads, junior developers, rapid prototyping

```bash
/plugin install fullstack-starter-pack@claude-code-plugins
```

---

### AI/ML Engineering Pack (12 plugins)

**Professional AI/ML engineering toolkit**

**Component Breakdown**:
- 01-prompt-engineering: 1 command, 2 agents
- 02-llm-integration: 1 command, 2 agents
- 03-rag-systems: 1 command, 2 agents
- 04-ai-safety: 1 command, 2 agents

**Total**: 4 commands, 8 agents

**Features**:
- Prompt optimization and A/B testing (30-50% cost reduction)
- Multi-provider LLM integration and model evaluation
- RAG system design and vector database setup (Pinecone, Weaviate)
- AI safety guardrails and fine-tuning preparation
- Production-ready patterns for AI products

**Requirements**: Claude Code CLI, Anthropic or OpenAI API key

```bash
/plugin install ai-ml-engineering-pack@claude-code-plugins
```

---

## Example Use Cases

### For Developers

```bash
# Analyze your codebase health
/plugin install project-health-auditor@claude-code-plugins
/analyze /path/to/repo

# Debug API failures
/plugin install conversational-api-debugger@claude-code-plugins
/debug-api

# Build a knowledge base
/plugin install domain-memory-agent@claude-code-plugins

# Never write commit messages again
/plugin install git-commit-smart@claude-code-plugins
/gc
```

### For Teams

Share custom workflows across your organization:

```json
// .claude/settings.json
{
  "extraKnownMarketplaces": {
    "claude-code-plugins": {
      "source": {
        "source": "github",
        "repo": "kimgyurae/claude-code-plugins"
      }
    }
  },
  "enabledPlugins": {
    "project-health-auditor@claude-code-plugins": true,
    "conversational-api-debugger@claude-code-plugins": true
  }
}
```

### For Plugin Creators

Use our templates to build your own plugins:

```bash
# Copy a template
cp -r templates/command-plugin my-awesome-plugin

# Customize and test locally
/plugin marketplace add ./my-test-marketplace
/plugin install my-awesome-plugin@test
```

---

## Documentation

### Getting Started
- [Installation & Usage](docs/getting-started.md) - Install and use plugins
- [Creating Your First Plugin](docs/creating-plugins.md) - Step-by-step tutorial
- [Plugin Reference](docs/plugin-structure.md) - Technical specifications

### Advanced Topics
- [Marketplace Guide](docs/marketplace-guide.md) - Distribute your plugins
- [Security Best Practices](docs/security-best-practices.md) - Secure plugin development
- [MCP Server Status](./MCP-SERVERS-STATUS.md) - MCP plugin configurations

---

## Contributing

We welcome community plugin submissions! This ecosystem thrives on shared knowledge and collaboration.

### Submit Your Plugin

1. **Fork** this repository
2. **Add** your plugin to `plugins/community/your-plugin/`
3. **Update** `.claude-plugin/marketplace.json` with your plugin entry
4. **Submit** a pull request using our plugin submission template

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

### Plugin Requirements

- Valid `.claude-plugin/plugin.json`
- Comprehensive README.md with examples
- LICENSE file (MIT or Apache-2.0 recommended)
- Tested locally and working
- No hardcoded secrets or credentials
- All scripts executable (`chmod +x`)

---

## Important Notes

### Not on GitHub Marketplace

**Claude Code plugins do NOT use GitHub Marketplace.** They operate in a completely separate ecosystem using JSON-based marketplace catalogs hosted in Git repositories. This repository IS a Claude Code plugin marketplace.

### No Built-in Monetization

**There is currently no monetization mechanism** for Claude Code plugins. All plugins in the ecosystem are free and open-source. See [Monetization Alternatives](docs/monetization-alternatives.md) for external revenue strategies.

### Beta Status

Claude Code plugins are in **public beta** (October 2025). Features and best practices may evolve. This marketplace will stay updated with the latest changes.

---

## Plugin Templates

Start building your own plugin today:

| Template | What's Included | Best For |
|----------|----------------|----------|
| **minimal-plugin** | Just plugin.json & README | Simple utilities |
| **command-plugin** | Slash commands | Custom workflows |
| **agent-plugin** | Specialized AI agent | Domain expertise |
| **full-plugin** | Commands + agents + hooks | Complex automation |

All templates are in the [`templates/`](templates/) directory with complete examples.

---

## Resources

### Official

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code/)
- [Plugin Guide](https://docs.claude.com/en/docs/claude-code/plugins)
- [Plugin Reference](https://docs.claude.com/en/docs/claude-code/plugins-reference)
- [Announcement Blog](https://www.anthropic.com/news/claude-code-plugins)
- [Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)

### Community

- [Claude Developers Discord](https://discord.com/invite/6PPFFzqPDZ) - 40,000+ members
- [Report Issues](https://github.com/kimgyurae/claude-code-plugins/issues)
- [Discussions](https://github.com/kimgyurae/claude-code-plugins/discussions)
- [Awesome Claude Code](https://github.com/hesreallyhim/awesome-claude-code) - Curated resources

### Other Marketplaces

- [Dan Ávila's Marketplace](https://github.com/davila7/claude-code-marketplace) - DevOps & productivity
- [Seth Hobson's Agents](https://github.com/wshobson/agents) - 80+ specialized subagents
- [CCPlugins](https://github.com/brennercruvinel/CCPlugins) - Professional commands

---

## Statistics

- **Plugin Packs**: 4 (62 total plugin components)
- **MCP Plugins**: 5 (21 total MCP tools)
- **Production Plugins**: 2 (git-commit-smart, overnight-dev)
- **AI Agency Plugins**: 6 (complete business toolkit)
- **Example Plugins**: 3 (hello-world, formatter, security-agent)
- **Templates**: 4 (minimal, command, agent, full)
- **Total Marketplace Plugins**: 20

---

## Our Mission

To be **THE definitive resource** for Claude Code plugins by:

1. **Educating** - Clear examples showing how plugins work
2. **Curating** - High-quality plugins you can trust
3. **Connecting** - Building a vibrant community of creators
4. **Growing** - Setting standards as the ecosystem evolves

---

## Why This Marketplace?

- **Quality over Quantity** - Every plugin is reviewed and tested
- **Learning-Focused** - Understand how plugins work, don't just use them
- **First-Mover** - Establishing best practices for the ecosystem
- **Community-Driven** - Built by developers, for developers
- **Actively Maintained** - Updated with latest Claude Code features

---

## License

MIT License - See [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **Anthropic** - For creating Claude Code and the plugin system
- **Community Contributors** - Everyone who submits plugins and improvements
- **Early Adopters** - Users who provide feedback and help us improve

---

## 💬 Community

Join the conversation and connect with other plugin developers and users!

### Discussions
- **[General Discussions](https://github.com/kimgyurae/claude-code-plugins/discussions)** - Community hub for all things plugins
- **[Announcements](https://github.com/kimgyurae/claude-code-plugins/discussions/categories/announcements)** - Stay updated with the latest releases
- **[Ideas](https://github.com/kimgyurae/claude-code-plugins/discussions/categories/ideas)** - Suggest new plugins or features
- **[Q&A](https://github.com/kimgyurae/claude-code-plugins/discussions/categories/q-a)** - Get help from the community
- **[Show and Tell](https://github.com/kimgyurae/claude-code-plugins/discussions/categories/show-and-tell)** - Share what you've built!

### Other Channels
- **[Discord](https://discord.com/invite/6PPFFzqPDZ)** - Claude Code Community (#claude-code channel)
- **[Issues](https://github.com/kimgyurae/claude-code-plugins/issues)** - Report bugs or request features
- **[Pull Requests](https://github.com/kimgyurae/claude-code-plugins/pulls)** - Contribute your own plugins

---

## Get Help

- **Questions?** - [Open a discussion](https://github.com/kimgyurae/claude-code-plugins/discussions/categories/q-a)
- **Found a bug?** - [Report an issue](https://github.com/kimgyurae/claude-code-plugins/issues)
- **Have an idea?** - [Share in Ideas](https://github.com/kimgyurae/claude-code-plugins/discussions/categories/ideas)
- **Want to chat?** - [Join our Discord](https://discord.com/invite/6PPFFzqPDZ)

---

<div align="center">

**[Star this repo](https://github.com/kimgyurae/claude-code-plugins)** if you find it useful!

Made with dedication by the Claude Code community

**[Get Started Now](#quick-start)** | **[Browse Plugins](#all-plugins)** | **[Contribute](#contributing)**

</div>

---

**Status**: Public Beta | **Version**: 3.1.0 | **Last Updated**: October 12, 2025
