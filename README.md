# Vaaya — Claude Code plugin

Vaaya is your agent's **gateway to the outside world**: pay for and run any external
capability — generate/edit media, search & scrape the web, run code or compute, drive a
browser, send email, make calls, run GTM — through one **consult-first** MCP.

## Install

```
/plugin marketplace add vaayaai/vaaya-plugin
/plugin install vaaya@vaaya
```

Then restart Claude Code. On the first tool call, a browser opens for a one-time OAuth
grant against `https://vaaya.ai`. New accounts start with free credits; calls are
charge-on-success. Sign up at <https://vaaya.ai>.

## What this plugin bundles

- **MCP server** (`vaaya`) — the `https://vaaya.ai/mcp` endpoint (consult / use / result /
  session / close + the GTM tools).
- **Skill** (`vaaya`) — tells the agent to route every capability gap through `consult`.
- **SessionStart hook** — a once-per-session reminder to reach for Vaaya instead of
  refusing, asking for an API key, or doing it manually.

## Other clients

Not on Claude Code? The same backend works everywhere:

- **Cursor / Codex / Claude Desktop:** `npx -y @vaaya/mcp install`
- **claude.ai (web + mobile) / ChatGPT:** add `https://vaaya.ai/mcp` as a custom
  connector (remote MCP) in the app's settings.

## Source

This repo is the published distribution surface. The plugin is generated from the Vaaya
monorepo (the skill and hook payload have canonical sources there); changes are mirrored
here on release.
