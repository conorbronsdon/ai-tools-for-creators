<div align="center">

# AI Tools for Creators

A curated collection of AI skills, MCP servers, and workflow tools for content creators.

[![GitHub stars](https://img.shields.io/github/stars/conorbronsdon/ai-tools-for-creators?style=flat-square)](https://github.com/conorbronsdon/ai-tools-for-creators/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conor_Bronsdon-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/conorbronsdon/)
[![Podcast](https://img.shields.io/badge/Podcast-Chain_of_Thought-purple?style=flat-square)](https://chainofthought.show)
[![X](https://img.shields.io/badge/X-@ConorBronsworthy-black?style=flat-square&logo=x)](https://x.com/ConorBronsworthy)

</div>

---


This is a living collection. Some tools are mine, most are things I've found and vouch for. If something's here, I've used it or someone I trust has.

## Skills

**What's a skill?** A markdown file that teaches an AI coding agent how to do a specific task. Drop it into your project, and the agent follows the instructions. No code to install — just a file.

Drop-in instruction files for AI coding agents (Claude Code, Cursor, Windsurf, etc.). Copy the file, point your agent at it, done.

### Writing & Content

| Skill | What it does | Author |
|-------|-------------|--------|
| [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) | Comprehensive checklist for catching and fixing AI writing patterns. 90+ patterns across vocabulary, structure, rhythm, and more. | [@conorbronsdon](https://github.com/conorbronsdon) |

### Productivity & Workflow

| Skill | What it does | Author |
|-------|-------------|--------|
| [session-management](https://github.com/conorbronsdon/claude-code-skills/tree/master/session-management) | Four commands (/start, /end, /update, /today) that give Claude Code memory across sessions. State files, session logs, daily heartbeats. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [reconcile](https://github.com/conorbronsdon/claude-code-skills/tree/master/reconcile) | Tripwire check for multi-session drift — scans commits and state files for inconsistencies from parallel sessions. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [recover](https://github.com/conorbronsdon/claude-code-skills/tree/master/recover) | Scan for orphaned worktrees and stale branches after crashes. Read-only by default, cleanup requires approval. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [skill-creator](https://github.com/conorbronsdon/claude-code-skills/tree/master/skill-creator) | Generate new skills from plain-language descriptions. Scaffolds SKILL.md, command file, and CLAUDE.md additions. | [@conorbronsdon](https://github.com/conorbronsdon) |

## MCP Servers

**What's MCP?** Model Context Protocol — a standard way to connect AI agents to external tools and data (calendars, databases, APIs). Think of it as a USB-C port for AI.

MCP servers give AI agents access to real tools and data.

### Content & Publishing

| Server | What it does | Author |
|--------|-------------|--------|
| [Transistor-MCP](https://github.com/conorbronsdon/Transistor-MCP) | Full Transistor.fm API access — episodes, analytics, transcripts, show management. | [@conorbronsdon](https://github.com/conorbronsdon) (fork of [@gxjansen](https://github.com/gxjansen/Transistor-MCP)) |
| [substack-mcp](https://github.com/conorbronsdon/substack-mcp) | Read posts, manage drafts on Substack. No publish or delete by design — safe for agent workflows. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [podcastindex-mcp](https://github.com/conorbronsdon/podcastindex-mcp) | Podcast Index API — search by person/topic, trending podcasts, feed health checks, cross-platform episode discovery. | [@conorbronsdon](https://github.com/conorbronsdon) |

### Productivity & Workspace

| Server | What it does | Author |
|--------|-------------|--------|
| [gws-mcp-server](https://github.com/conorbronsdon/gws-mcp-server) | Google Workspace access — 24 tools across Drive, Sheets, Calendar, Docs, and Gmail. | [@conorbronsdon](https://github.com/conorbronsdon) |

## How to Use These

### Skills (Claude Code)

Most skills follow the [agentskills.io](https://agentskills.io) standard and work across tools. For Claude Code specifically:

1. Download the skill file (usually `SKILL.md` or similar)
2. Place it in your project directory or reference it in your CLAUDE.md
3. Invoke it — most skills include slash command instructions

### Skills (Other Agents)

Skills in the agentskills.io format work with Cursor, Windsurf, Cline, OpenHands, and 40+ other tools. Check each skill's README for tool-specific setup.

### MCP Servers

Each MCP server has its own install instructions. Generally:

1. Clone the repo
2. `npm install && npm run build`
3. Add the server to your Claude Code or Claude Desktop config

See Anthropic's [MCP documentation](https://modelcontextprotocol.io/) for setup details.

## Contributing

This is a curated list, not a dump. If you've built or found a tool that's genuinely useful for content creators, knowledge workers, or anyone who ships ideas for a living:

1. Open an issue describing the tool and why it's worth including
2. Or submit a PR adding it to the right section

Quality bar: you've actually used it, not just bookmarked it.

## About

Maintained by [Conor Bronsdon](https://github.com/conorbronsdon). I host the [Chain of Thought](https://chainofthought.show) podcast covering AI infrastructure, developer tools, and how practitioners actually use this stuff. Many of these tools were built or discovered through conversations with guests on the show.

New to AI tools? Check out [AI Learning Resources](https://github.com/conorbronsdon/ai-learning-resources) — a curated path from "what is AI?" to building your own workflows.

If you want to go deeper on any of these topics, the podcast is a good place to start.
