# Orlog MCP Server

Multi-perspective decision reasoning for Claude. When you're facing a real choice — career, money, relationships, strategy — Orlog examines the competing angles and takes a clear position, not a hedge.

**[Get an API key → orlog.fyi](https://orlog.fyi)**

---

## What it does

Two tools Claude can call:

| Tool | When Claude uses it |
|---|---|
| `orlog_decide` | User has a clear decision with real tension |
| `orlog_explore` | User is stuck or unsure what they're actually deciding |

Orlog doesn't hedge. It reasons through competing angles — what each side actually costs, what's really at stake, what the person is avoiding saying — and takes a position.

---

## Install

**Step 1 — Get an API key**

Sign up at [orlog.fyi](https://orlog.fyi) and get your key from the Developers page.

**Step 2 — Add to Claude config**

For Claude Desktop (`~/Library/Application Support/Claude/claude_desktop_config.json` on Mac, `%APPDATA%\Claude\claude_desktop_config.json` on Windows):

```json
{
  "mcpServers": {
    "orlog": {
      "type": "sse",
      "url": "https://tomsem77--mimir-mcp-serve.modal.run/sse",
      "headers": {
        "X-API-Key": "your-api-key-here"
      }
    }
  }
}
```

For Claude Code (add to your project or global `.claude/settings.json`):

```json
{
  "mcpServers": {
    "orlog": {
      "type": "sse",
      "url": "https://tomsem77--mimir-mcp-serve.modal.run/sse",
      "headers": {
        "X-API-Key": "your-api-key-here"
      }
    }
  }
}
```

**Step 3 — Restart Claude**

Orlog appears automatically. Claude will call it when you bring a real decision.

---

## Usage

You don't need to invoke Orlog manually. Just talk to Claude. When the conversation surfaces a real decision, Claude calls `orlog_decide` or `orlog_explore` automatically.

Or prompt it directly:
> *"Use Orlog to help me think through whether to take this job offer."*

---

## Pricing

| Tier | Calls/day | Price |
|---|---|---|
| Free | 10 | Free |
| Pro | 500 | $8/mo |

Get your key and manage billing at [orlog.fyi](https://orlog.fyi).

---

## About

Orlog is built on Mimir — a fine-tuned reasoning model trained specifically on decision quality, not general knowledge. The reasoning framework draws from multiple deliberative perspectives to surface what's actually at stake before taking a position.

Built by [Thomas Semrad](https://orlog.fyi).
