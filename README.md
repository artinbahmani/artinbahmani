# Artin Bahmani

Independent systems architect in Dubai. Local LLMs and AI automation, lead pipelines, messaging infrastructure, market-data systems, self-hosted platforms.

I design, build and operate production automation that real businesses run on every day. I run open-weight models locally on my own Apple Silicon production server (Ollama: Qwen3 14B, Llama 3.2 3B, nomic-embed-text embeddings, with RAG on PostgreSQL pgvector), and I use frontier LLM APIs (Anthropic Claude) in production.

Most of my work lives in private production repos. The case studies below document the architecture, design decisions and selected code from systems that are live right now.

## Featured work

| Project | What it is |
|---|---|
| [realestate-agent-portal](https://github.com/artinbahmani/realestate-agent-portal) | Operations platform for a Dubai real-estate brokerage. Real-time lead pipeline, campaign attribution, agent dashboards. |
| [rtb-market-daemon](https://github.com/artinbahmani/rtb-market-daemon) | 24/7 crypto market-data daemon. Three exchanges, news ingestion, TimescaleDB, alerting. |
| Messaging engine (private) | Compliance-first business messaging engine with a human approval gate before every send. 35% reply rate. Source is private. Demo on request. |
| [selfhosted-ai-stack](https://github.com/artinbahmani/selfhosted-ai-stack) | Self-hosted production stack on Apple Silicon. Docker, Postgres, RAG, backups, monitoring. |
| [pg-docker-backup](https://github.com/artinbahmani/pg-docker-backup) | Nightly backups for Postgres running in Docker, with rotation and restore verification. |
| [heartbeat-watchdog](https://github.com/artinbahmani/heartbeat-watchdog) | Wrap any script or cron job with heartbeat monitoring and Telegram failure alerts. |
| [rss-telegram-watcher](https://github.com/artinbahmani/rss-telegram-watcher) | Polls RSS feeds with jitter, dedupes, and pushes new items to Telegram. |

### Messaging engine (private)

A compliance-first business messaging engine built around one rule: no message is sent without a human approving it.

- A human approval gate comes before any message is sent.
- Per-sender daily caps with a warm-up ramp.
- Randomized send timing with rest periods.
- Sender health and eligibility checks before every batch.
- Opt-out is honored immediately and permanently through a suppression list.
- Replies are detected and routed to the right person.
- Daily reporting to Telegram.
- Messages are drafted by an LLM, then a human edits or approves them.

**Result:** 35% reply rate.

Source is private. Demo on request.

## Featured live demos

Limited demo versions of browser-only apps with no server and no API keys: real-estate and market tools built on official and public data, plus a game built from scratch on canvas. All demos in one place: [artinbahmani.artin-bahmani0.workers.dev](https://artinbahmani.artin-bahmani0.workers.dev/). Full versions on request.

| App | Try it | What it is |
|---|---|---|
| [dubai-transactions-map](https://github.com/artinbahmani/dubai-transactions-map) | [open](https://artinbahmani.artin-bahmani0.workers.dev/dubai-transactions-map/) | Interactive map of Dubai property transactions from official Land Department open data. Color-coded communities, price per sqm, click any area for full stats. |
| [chart-studio](https://github.com/artinbahmani/chart-studio) | [open](https://artinbahmani.artin-bahmani0.workers.dev/chart-studio/) | Browser-only trading chart studio: six exchange datafeeds, dozens of indicators, pattern markers, bar replay, shareable state. |
| [derivatives-radar](https://github.com/artinbahmani/derivatives-radar) | [open](https://artinbahmani.artin-bahmani0.workers.dev/derivatives-radar/) | Keyless crypto derivatives terminal: funding APY across exchanges, open interest, long/short ratios, Fear and Greed history. |
| [crypto-screener](https://github.com/artinbahmani/crypto-screener) | [open](https://artinbahmani.artin-bahmani0.workers.dev/crypto-screener/) | Screener over every Binance pair with preset screens, composable conditions, sparklines and CSV export. |
| [rts-skirmish](https://github.com/artinbahmani/rts-skirmish) | [play](https://artinbahmani.artin-bahmani0.workers.dev/rts-skirmish/) | Real-time strategy skirmish: gather, build, upgrade, and destroy the enemy base against an AI. Canvas, no engine and no dependencies. |

Also built: [Dubai Estate Suite](https://github.com/artinbahmani/dubai-estate-suite), [Dubai property calculators](https://github.com/artinbahmani/dubai-property-calculators), [a Dubai mortgage calculator](https://github.com/artinbahmani/dubai-mortgage-calculator), [a POS storefront](https://github.com/artinbahmani/pos-storefront), [an invoice generator](https://github.com/artinbahmani/invoice-generator), [an expense tracker](https://github.com/artinbahmani/expense-tracker), [a habit tracker](https://github.com/artinbahmani/habit-tracker) and [a crypto ticker](https://github.com/artinbahmani/crypto-ticker), plus canvas games ([tower defense](https://github.com/artinbahmani/tower-defense), [space shooter](https://github.com/artinbahmani/space-shooter), [merchant tycoon](https://github.com/artinbahmani/merchant-tycoon), [gem crush](https://github.com/artinbahmani/gem-crush), [brick breaker](https://github.com/artinbahmani/brick-breaker), [sudoku](https://github.com/artinbahmani/sudoku), [snake arcade](https://github.com/artinbahmani/snake-arcade), [tower stack](https://github.com/artinbahmani/tower-stack), [minesweeper](https://github.com/artinbahmani/minesweeper)).

## How I work

I care about systems that keep running when nobody is watching. That means idempotent pipelines, dedup at every ingestion point, heartbeat monitors on every long-running process, alerting that reaches my phone, and backups that get restore-tested instead of just written to disk.

## Stack

- **Languages:** Python, JavaScript / Node.js, SQL, Bash
- **AI:** Ollama with open-weight models (Qwen3 14B, Llama 3.2 3B), nomic-embed-text embeddings, RAG on PostgreSQL pgvector, frontier LLM APIs (Anthropic Claude) in production
- **Data:** PostgreSQL (TimescaleDB, pgvector), Redis, Airtable
- **Infra:** Docker Compose, Tailscale, Cloudflare, Uptime Kuma, self-hosted n8n
- **Integrations:** messaging APIs (WhatsApp, Telegram), exchange websockets (Bybit, Binance, Hyperliquid)
- **Web:** Webflow, no-code front-ends wired to custom backends

## Now

Building a real-time trading intelligence platform: whale tracking on Hyperliquid, multi-timeframe market analysis, and a command-center dashboard, all running on my own local infrastructure.

## Work with me

The source code of my production systems is private. To use any of these systems or to get a full version, contact me at artin.bahmani0@gmail.com or on [LinkedIn](https://www.linkedin.com/in/artin-bahmani-6148b433b).

📍 Dubai, UAE · 📫 artin.bahmani0@gmail.com · [LinkedIn](https://www.linkedin.com/in/artin-bahmani-6148b433b)
