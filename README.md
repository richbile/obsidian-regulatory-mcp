# Obsidian Regulatory MCP

> The verified, tier-0 regulatory data layer for your AI. Connect Claude, ChatGPT, or Cursor to official regulatory data, with a source, date, and status on every answer.

[![Website](https://img.shields.io/badge/website-obsidianri.com%2Fmcp-2B7AE4)](https://obsidianri.com/mcp)
[![MCP](https://img.shields.io/badge/Model%20Context%20Protocol-server-111827)](https://modelcontextprotocol.io)
[![Free tier](https://img.shields.io/badge/free%20tier-no%20credit%20card-059669)](https://obsidianri.com/mcp)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

**Obsidian Regulatory MCP** is a [Model Context Protocol](https://modelcontextprotocol.io) server that gives AI assistants real-time access to verified regulatory data from **850+ official, tier-0 sources across 50+ jurisdictions** (Chemicals, ESG, Life Sciences). It is the missing data layer that stops AI from hallucinating on regulation.

- 🌐 **Website and access:** https://obsidianri.com/mcp
- 🟢 **Status:** live. Sign in with Obsidian (OAuth 2.1), no API key. Free tier, no credit card.

---

## Why this exists

Frontier models reason brilliantly but guess on regulation: hallucinated citations, stale texts, and no way to tell a draft from a law in force. In compliance, a confident wrong answer is a liability.

The fix is not a smarter model, it is a verified source of truth the model can call. **You already have the intelligence. Obsidian brings the data.**

Read the thesis: [Agentic Regulatory Intelligence](https://obsidianri.com/blog/agentic-regulatory-intelligence) · [Why AI Hallucinates on Regulatory Questions](https://obsidianri.com/blog/why-ai-hallucinates-regulatory-questions) · [RAG vs MCP](https://obsidianri.com/blog/rag-vs-mcp-regulatory-ai) · [What Tier-0 Regulatory Data Means](https://obsidianri.com/blog/tier-0-regulatory-data-explained)

## Works with

Claude (Desktop and Claude Code), Cursor, and any MCP-compatible client. ChatGPT and Perplexity as MCP support rolls out across them.

## Quickstart

**No API key to copy.** Add the connector URL; on first use your assistant opens a browser to sign in with Obsidian (OAuth 2.1). New accounts get the free tier automatically. Full walkthrough: [How to Connect a Regulatory MCP to Claude](https://obsidianri.com/blog/how-to-connect-regulatory-mcp-to-claude).

### Claude Desktop / Cursor

Add a custom connector pointing at:

```
https://mcp.obsidianri.com/sse
```

No auth headers needed: the client discovers the OAuth flow automatically and prompts you to sign in.

### Claude Code

```bash
claude mcp add --transport sse obsidian-regulatory https://mcp.obsidianri.com/sse
```

Then authorize in the browser when prompted. See also [`examples/`](examples/) for raw config.

> Auth is OAuth 2.1 (sign in with your Obsidian account). The free tier needs no credit card.

## What you get

- **850+ official, tier-0 sources** across 50+ jurisdictions (EU, US, UK, CH, APAC, and more)
- Every result returned with its **source, date, jurisdiction, framework, and status**
- Coverage of REACH, CLP, TSCA, CSRD, ESRS, EU Taxonomy, CS3D, MDR, IVDR, FDA 21 CFR, the AI Act, and more
- **Free tier**: 100 verified requests per month, no credit card

## Example tools

The server exposes structured tools your assistant calls in natural language:

| Tool | What it does |
|------|--------------|
| `regulatory_search` | Semantic search across verified, tier-0 official regulations, filtered by jurisdiction, framework, topic, and date. Every result carries its official source, date, and status. |
| `search_news` | Keyword search across regulatory news and updates, returning title, official source, and date. |

Plus helper tools for frameworks, industries, official sources, and the latest regulatory news.

## Example prompts

```
"What changed on CSRD reporting this month? EU only, top 3, with source and date."
"Is this substance on the REACH Candidate List, and restricted in the EU and US?"
"What MDR transition deadlines apply to a Class IIb device?"
```

More: [Regulatory Research Prompts That Work](https://obsidianri.com/blog/claude-obsidian-mcp-regulatory-research-prompts) · [Building an Agentic Compliance Workflow](https://obsidianri.com/blog/agentic-compliance-workflow-claude-mcp)

## Get access

Just add the connector and sign in with your Obsidian account, no API key to copy. Free tier, no credit card. Learn more at **[obsidianri.com/mcp](https://obsidianri.com/mcp)**.

## About

Built by [Obsidian Regulatory Intelligence](https://obsidianri.com), which continuously monitors official regulatory sources worldwide for compliance, legal, and strategy teams.

## License

MIT (documentation and configuration examples). See [LICENSE](LICENSE).
