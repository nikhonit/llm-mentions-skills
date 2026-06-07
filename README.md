# llm-mentions-skills

**Agent skills for AI brand-visibility tracking.** Drop-in skills that let any agent check whether a brand is mentioned, ranked, and cited across ChatGPT, Claude, Gemini, Perplexity, Google AI Overviews, Google AI Mode, and Bing Copilot — over the [MentionsAPI REST API](https://mentionsapi.com).

Free to start — [grab a key](https://mentionsapi.com/signup) ($1 free credit, no card required) and you're measuring AI visibility from Claude, ChatGPT, Cursor, or your own agent loop in under two minutes.

Pure Python standard library. No dependencies. MIT-0 licensed.

## Install

```bash
# OpenClaw (via ClawHub)
npx clawhub@latest install mentions-full

# Hermes Agent
hermes skills install skills-sh/nikhonit/llm-mentions-skills/skills/mentions-full

# Generic agent skills (Claude Code, Cursor, Cline)
npx skills add nikhonit/llm-mentions-skills
```

## Skills in this repo

| Skill | Purpose | Cost |
|---|---|---|
| [`mentions-full`](skills/mentions-full) | Complete AI-visibility toolkit — check mentions, discover queries, compare brands, watch for changes | from $0.02/call |
| [`mentions-check`](skills/mentions-check) | Single-call brand-visibility check across 8 AI surfaces | from $0.02/call |
| [`mentions-discover`](skills/mentions-discover) | Suggest ~50 queries worth tracking for a brand | $0.50/call |

Install the bundled `mentions-full` for agents that need broad coverage. Install the focused variants when you want minimum tool surface.

## Authentication

Set the `MENTIONSAPI_KEY` environment variable to your MentionsAPI key (format `lvk_live_...`).

```bash
export MENTIONSAPI_KEY="lvk_live_..."
```

**[Get a free key in 30 seconds](https://mentionsapi.com/signup)** — $1 free credit, no card required. The same key works for these skills, the [hosted MCP server](https://www.npmjs.com/package/@mentionsapi/mcp), and direct REST calls.

## Pricing

**Pay-as-you-go. No subscriptions, no monthly tiers, credits never expire.**

- **$1 free signup credit** — no card required
- **$5 minimum top-up** — wallet balance, billed per call in real time

| `mentions_check` mode | Cost | What it hits |
|---|---|---|
| `quick` | $0.02 | All 4 LLM APIs in parallel (ChatGPT, Claude, Gemini, Perplexity) |
| `ai_overview` | $0.05 | Google AI Overviews block |
| `bing_copilot` | $0.05 | Bing Copilot |
| `chatgpt_live` | $0.10 | Live ChatGPT UI scrape (fan-out + entities) |
| `gemini_live` | $0.10 | Live Gemini UI scrape |
| `ai_mode` | $0.10 | Google AI Mode |
| `perplexity_live` | $0.25 | Live Perplexity UI scrape (citations + fan-out) |
| `all_live` | $0.50 | All 6 live UI surfaces in one call |

Other tools: `discover` $0.50/call · `compare` $1.50/call · `watch` $1/run. Failed calls are not billed.

## Source

- API reference: <https://mentionsapi.com/docs/api/check> · OpenAPI: <https://mentionsapi.com/openapi.json>
- Hosted MCP server (alternative to these skills): `npx @mentionsapi/mcp`
- Quickstart: <https://mentionsapi.com/docs/quickstart>

## Issues and contributions

See [CONTRIBUTING.md](CONTRIBUTING.md). Security reports: [SECURITY.md](SECURITY.md).

## License

[MIT No Attribution](LICENSE). Fork, ship, sublicense — no attribution required.

## Independence and trademarks

MentionsAPI is an independent service and is not affiliated with, endorsed by, or sponsored by OpenAI, Anthropic, Google, Microsoft, or Perplexity. "ChatGPT" is a trademark of OpenAI; "Claude" of Anthropic; "Gemini" and "AI Overviews" of Google; "Copilot" of Microsoft; "Perplexity" of Perplexity AI. All product names are the property of their respective owners.
