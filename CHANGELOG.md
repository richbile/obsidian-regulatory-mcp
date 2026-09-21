# Changelog

All notable changes to the Obsidian Regulatory MCP connector are documented here.
Versions follow the `version` field of `server.json`.

## [0.1.0] - 2026-09-21

First tagged release of the connector repository.

### Server (live at `https://mcp.obsidianri.com/mcp`)
- Transport: Streamable HTTP on `/mcp` (the deprecated `/sse` endpoint was removed).
- Auth: OAuth 2.1, sign in with your Obsidian account, no API key. Free tier, no credit card.
- Tools exposed: `regulatory_search`, `search_enforcement`, `standards_lookup`, `search_news`.

### Repository
- `glama.json` declaring the maintainer for the Glama listing.
- README: tool table now lists all four tools with their scope.
- Open Plugins manifest (`mcp.json` + `.plugin/plugin.json`) for the Cursor directory.
- `server.json` aligned with the MCP registry schema (2025-12-11).
