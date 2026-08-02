<div align="center">

# AI Tools for Creators

A curated collection of AI skills, MCP servers, and workflow tools for content creators.

[![GitHub stars](https://img.shields.io/github/stars/conorbronsdon/ai-tools-for-creators?style=social&cacheSeconds=3600)](https://github.com/conorbronsdon/ai-tools-for-creators/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Podcast](https://img.shields.io/badge/Podcast-Chain_of_Thought-purple?style=flat-square)](https://chainofthought.show/?utm_source=github&utm_medium=referral&utm_campaign=repo-readme&utm_content=ai-tools-for-creators)
[![X](https://img.shields.io/badge/X-@ConorBronsdon-black?style=flat-square&logo=x)](https://x.com/ConorBronsdon)

</div>

---


This is a living collection. Some tools are mine, most are things I've found and vouch for. If something's here, I've used it or someone I trust has.

## Skills

**What's a skill?** A markdown file that teaches an AI coding agent how to do a specific task. Drop it into your project, and the agent follows the instructions. No code to install — just a file.

Drop-in instruction files for AI coding agents (Claude Code, Cursor, Windsurf, etc.). Copy the file, point your agent at it, done.

### Writing & Content

| Skill | What it does | Author |
|-------|-------------|--------|
| [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) | Audit & rewrite content to remove AI writing patterns — 53 pattern categories + a 109-entry replacement table. Rewrite / detect / edit-in-place modes, optional voice profiles (casual/professional/technical/warm/blunt), and a zero-dependency detector engine. Installs as a Claude Code / Cowork plugin or a standalone skill. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [demo-gif-skill](https://github.com/conorbronsdon/demo-gif-skill) | Add a reproducible demo GIF to any repo's README in one prompt. Picks the method (vhs for terminals, Playwright for web apps), writes a committed recording script so the GIF regenerates instead of going stale, optimizes under 8 MB, and embeds it with real alt text. Works in Claude Code and any agentskills.io agent. | [@conorbronsdon](https://github.com/conorbronsdon) |

### Productivity & Workflow

| Skill | What it does | Author |
|-------|-------------|--------|
| [agent-workspace](https://github.com/conorbronsdon/agent-workspace) | Memory and hygiene for agent workspaces — six lifecycle skills (/start, /end, /update, /today, /reconcile, /recover) with a configurable state layout. State files, session logs, daily heartbeats, drift and worktree cleanup. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [reconcile](https://github.com/conorbronsdon/agent-workspace) | Tripwire check for multi-session drift — scans commits and state files for inconsistencies from parallel sessions. Part of agent-workspace. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [recover](https://github.com/conorbronsdon/agent-workspace) | Scan for orphaned worktrees and stale branches after crashes. Read-only by default, cleanup requires approval. Part of agent-workspace. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [agent-skill-builder](https://github.com/conorbronsdon/agent-skill-builder) | Build agent skills that don't rot. Generates skills from plain-language descriptions with the design decisions most generators skip (invocation control, arguments, context budget), validates them with a bundled checker, and pins its spec knowledge to a CI-watched snapshot. New/review/migrate modes. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [ssot-check](https://github.com/conorbronsdon/ssot-check) | Single-source-of-truth drift auditor, now tool-backed: deterministic stdlib CLI (45 tests) + skill wrapper + pre-commit hook + GitHub Action. Finds facts hand-copied across docs, builds a manifest of canonical locations, and flags every copy that drifted. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [repo-audit](https://github.com/conorbronsdon/repo-audit) | Audit a repo against its own code, or get it ready to open-source. For every claim that something is prevented, blocked, or guaranteed, it finds the mechanism and grades it Enforced, Advisory, or Guidance — a warning that prints but does not block is not enforcement. Reads source, tests, hooks and CI before the README; every finding cites file:line and what it could not verify. Six checklist packs, five README templates, optional modules. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [agent-memory-kit](https://github.com/conorbronsdon/agent-memory-kit) | The curation loop for agent memory — capture, recall, and a read-only curator that finds rot and contradictions before your agent is confidently wrong. Plain markdown and JSON, five slash commands, human-reviewed diffs. | [@conorbronsdon](https://github.com/conorbronsdon) |

### Development & Code Review

| Skill | What it does | Author |
|-------|-------------|--------|
| [code-review](https://github.com/conorbronsdon/claude-code-skills/tree/main/code-review) | Multi-agent PR review — orchestrates Copilot + parallel subagents (adversarial, operational, reference-comparison) sized to PR risk. Catches architectural P0s that single-pass review misses. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [eval-integrity](https://github.com/conorbronsdon/eval-integrity) | Audit an LLM benchmark repo for credibility practices — 36 scoreable sub-checks across seven dimensions, a JSON result schema for CI, and three audit fixtures. Answers: would your published numbers survive an adversarial reviewer? | [@conorbronsdon](https://github.com/conorbronsdon) |
| [readme-audit](https://github.com/nnennandukwe/skills/tree/main/skills/readme-audit) | Audit a README against what the software actually does. Reads the CLI help, schemas, and parity tests first, then reports P1/P2/P3 findings with the evidence checked and the sources it couldn't verify. Fails a README that claims enforcement without naming the mechanism doing it. Read-only unless you ask for a rewrite. Part of [nnennandukwe/skills](https://github.com/nnennandukwe/skills). | [@nnennandukwe](https://github.com/nnennandukwe) |
| [software-build-plan](https://github.com/nnennandukwe/skills/tree/main/skills/software-build-plan) | Turn one ticket into an implementation-ready plan — contracts, file seams, commit sequence, test plan — before any code is written. Its pre-PR gate requires a second review from a different model family, pinned by model id, because a second pass from the same family shares its blind spots. Part of [nnennandukwe/skills](https://github.com/nnennandukwe/skills). | [@nnennandukwe](https://github.com/nnennandukwe) |
| [failure-path-testing](https://github.com/nnennandukwe/skills/tree/main/skills/failure-path-testing) | Write the failure test first — start from the transition that must stay blocked, the gate that must refuse, the empty config that must fail loudly instead of resolving to a wrong default. Part of [nnennandukwe/skills](https://github.com/nnennandukwe/skills). | [@nnennandukwe](https://github.com/nnennandukwe) |

### Research & Booking

| Skill | What it does | Author |
|-------|-------------|--------|
| [angel-diligence](https://github.com/conorbronsdon/claude-code-skills/tree/main/angel-diligence) | Pre-investment research and deal-memo generation. Parallel web research with strict citation rules; separates verified facts from claims; ends in a verdict scaffold, never an invest/pass call. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [guest-circuit](https://github.com/conorbronsdon/claude-code-skills/tree/main/guest-circuit) | Map a prospective podcast guest's appearance circuit — where they've been, their stump speech, and the unclaimed angle for your show. Uses Podcast Index when configured, web search otherwise. | [@conorbronsdon](https://github.com/conorbronsdon) |

## MCP Servers

**What's MCP?** Model Context Protocol — a standard way to connect AI agents to external tools and data (calendars, databases, APIs). Think of it as a USB-C port for AI.

MCP servers give AI agents access to real tools and data.

### Content & Publishing

| Server | What it does | Author |
|--------|-------------|--------|
| [Transistor-MCP](https://github.com/conorbronsdon/Transistor-MCP) | Full Transistor.fm API access — episodes, analytics, transcripts, show management. | [@conorbronsdon](https://github.com/conorbronsdon) (fork of [@gxjansen](https://github.com/gxjansen/Transistor-MCP)) |
| [substack-mcp](https://github.com/conorbronsdon/substack-mcp) | Read posts, manage drafts on Substack. No publish or delete by design — safe for agent workflows. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [podcastindex-mcp](https://github.com/conorbronsdon/podcastindex-mcp) | Podcast Index API — search by person/topic, trending podcasts, feed health checks, cross-platform episode discovery. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [op3-mcp](https://github.com/conorbronsdon/op3-mcp) | OP3 (Open Podcast Prefix Project) analytics — downloads over time, listener geography, app share, per-episode breakdowns. Read-only by design. | [@conorbronsdon](https://github.com/conorbronsdon) |

### Productivity & Workspace

| Server | What it does | Author |
|--------|-------------|--------|
| [gws-mcp-server](https://github.com/conorbronsdon/gws-mcp-server) | Google Workspace access — 39 curated tools across Gmail, Calendar, Drive, Sheets, Docs, and Tasks. Built on the official `gws` CLI. | [@conorbronsdon](https://github.com/conorbronsdon) |

### Social & Distribution

Publishing and scheduling across social platforms. Read the gating notes below before you plan a workflow around any of these — the API is rarely the hard part.

| Server | What it does | Author |
|--------|-------------|--------|
| [X MCP](https://docs.x.com/tools/mcp) | Official hosted MCP at `api.x.com/mcp`. Full-archive search, post and engagement lookup, user timelines, bookmarks, trends, and X Articles drafting. OAuth 2.0 via the `xurl` bridge for user-context writes, or an app-only bearer token for read-only. | [@XDevelopers](https://github.com/xdevplatform) |
| [Postiz](https://github.com/gitroomhq/postiz-app) | Self-hosted scheduler covering 32 networks including TikTok, Instagram, Threads, Bluesky, and Mastodon. A documented public API (`POST /posts`, `POST /upload`, `GET /integrations`) plus a Node SDK make it scriptable. **You still supply your own developer credentials per platform** — the compose file takes `TIKTOK_CLIENT_ID`, `THREADS_APP_ID`, `LINKEDIN_CLIENT_ID` and the rest, so it removes the integration work but not the app-review work. Runs on 2GB RAM / 2 vCPU. No MCP server. AGPL-3.0. | [@gitroomhq](https://github.com/gitroomhq) |
| [atproto-mcp](https://github.com/cameronrye/atproto-mcp) | Bluesky and the wider AT Protocol — 51 tools covering posts, threads, feeds, search, lists, DMs, and moderation. Runs read-only with zero config (`npx atproto-mcp`), or add an app password for writes. Every tool declares MCP annotations and destructive operations are flagged, which is rarer than it should be. Built on the official `@atproto/api` and MCP SDK, with rate limiting. MIT. | [@cameronrye](https://github.com/cameronrye) |
| [meta-mcp](https://github.com/mikusnuz/meta-mcp) | Instagram Graph API and Threads API in one server — 57 tools on Graph API v25.0. Publishes photos, videos, reels, stories, and carousels to Instagram; text, polls, GIFs, and carousels to Threads. Includes insights, comment management, and a cross-posting prompt. | [@mikusnuz](https://github.com/mikusnuz) |

**What actually gates you.** Posting is the last mile and the easy part. The work is upstream, and no scheduler removes it — self-hosted tools take your credentials, they don't lend you theirs:

- **TikTok** — personal accounts cannot use the Content Posting API. You need a business or developer entity, plus app review with a privacy policy and a demo video of your OAuth and upload flow. Budget 5–10 business days for approval.
- **Instagram** — Graph API publishing needs a Business or Creator account and a linked Facebook Page. Verify which account type your workflow requires before you commit; the answer has moved more than once.
- **Threads** — free API, and since September 2025 it no longer requires a linked Instagram account. Production access still waits on Meta App Review.
- **LinkedIn** — the most restrictive of the major platforms. Publishing runs through the Community Management API, which needs a registered company, a verified Page, and a two-tier app review. There is no quick path for individual developers.
- **Bluesky** — the exception. App passwords, no review, no paid tier, open protocol. If you want one platform automated this week, it's this one.

**Known gap:** there's no MCP server for Postiz. The public API is well-shaped and does the hard part already, so a wrapper would put 32 platforms behind one agent-facing interface.

**On finding the Bluesky one.** Searching GitHub for a Bluesky MCP returns a dozen-plus results, and sorting by stars is actively misleading here — the most-starred was last touched in April 2025. `atproto-mcp` sits at single-digit stars and is the only one that's actually maintained, published to npm, and annotated properly. Worth remembering when a category looks abandoned: it may just be badly sorted.

## Benchmarks & Evaluation

If you're building with agents, you eventually need to measure them. Tools for that:

| Project | What it does | Author |
|---------|-------------|--------|
| [cot-bench](https://github.com/conorbronsdon/cot-bench) | Open agent evaluation leaderboard. Three judges score every scenario (two open-weight, one frontier reference) across CLEAR-aligned metrics: efficacy, cost, reliability, latency. Rubrics are code, and every raw judge score is published so you can audit the results. | [@conorbronsdon](https://github.com/conorbronsdon) |
| [podcast-benchmark](https://github.com/conorbronsdon/podcast-benchmark) | Benchmark any podcast against its peers using only public data — catalog depth, cadence, transcript availability, feed hygiene. No download estimates, every number sourced and timestamped. | [@conorbronsdon](https://github.com/conorbronsdon) |

## Web Apps

Standalone tools that run in the browser. No agent, no install.

| App | What it does | Author |
|-----|-------------|--------|
| [track-finder](https://github.com/conorbronsdon/track-finder) | Paste a tracklist or a YouTube playlist URL and get search links for every track on SoundCloud, Spotify, YouTube, Apple Music, or Beatport. Progress saves in your browser. Built for DJs and playlist builders. | [@conorbronsdon](https://github.com/conorbronsdon) |

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

Maintained by [Conor Bronsdon](https://github.com/conorbronsdon). I host the [Chain of Thought](https://chainofthought.show/?utm_source=github&utm_medium=referral&utm_campaign=repo-readme&utm_content=ai-tools-for-creators) podcast covering AI infrastructure, developer tools, and how practitioners actually use this stuff. Many of these tools were built or discovered through conversations with guests on the show.

New to AI tools? Check out [AI Learning Resources](https://github.com/conorbronsdon/ai-learning-resources) — a curated path from "what is AI?" to building your own workflows.

If you want to go deeper on any of these topics, the podcast is a good place to start.

---

## Disclaimer

*This is an independent personal project, not affiliated with, sponsored by, or endorsed by any company. All views expressed are my own.*

## License

MIT (see [LICENSE](LICENSE)).
