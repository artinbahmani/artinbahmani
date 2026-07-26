# Artin Bahmani

Systems builder based in Dubai. I design, build and operate production automation: lead pipelines, messaging infrastructure, market-data systems, and self-hosted platforms that real businesses run on every day.

Most of my work lives in private production repos. The case studies below document the architecture, design decisions and selected code from systems that are live right now.

## Featured work

| Project | What it is |
|---|---|
| [realestate-agent-portal](https://github.com/artinbahmani/realestate-agent-portal) | Operations platform for a Dubai real-estate brokerage. Real-time lead pipeline, campaign attribution, agent dashboards. |
| [rtb-market-daemon](https://github.com/artinbahmani/rtb-market-daemon) | 24/7 crypto market-data daemon. Three exchanges, news ingestion, TimescaleDB, alerting. |
| [whatsapp-campaign-engine](https://github.com/artinbahmani/whatsapp-campaign-engine) | Compliance-first WhatsApp outreach engine with human approval gates and ban-safety design. |
| [selfhosted-ai-stack](https://github.com/artinbahmani/selfhosted-ai-stack) | Self-hosted production stack on Apple Silicon. Docker, Postgres, RAG, backups, monitoring. |
| [pg-docker-backup](https://github.com/artinbahmani/pg-docker-backup) | Nightly backups for Postgres running in Docker, with rotation and restore verification. |
| [heartbeat-watchdog](https://github.com/artinbahmani/heartbeat-watchdog) | Wrap any script or cron job with heartbeat monitoring and Telegram failure alerts. |
| [rss-telegram-watcher](https://github.com/artinbahmani/rss-telegram-watcher) | Polls RSS feeds with jitter, dedupes, and pushes new items to Telegram. |

## Playable demos

Small self-contained builds, each a single HTML file with no dependencies and a live demo on GitHub Pages:

| Demo | Try it | What it is |
|---|---|---|
| [tower-stack](https://github.com/artinbahmani/tower-stack) | [play](https://artinbahmani.github.io/tower-stack/) | Tower-stacking arcade game on a night skyline. Canvas, frame-rate independent. |
| [minesweeper](https://github.com/artinbahmani/minesweeper) | [play](https://artinbahmani.github.io/minesweeper/) | The classic, dark UI, first click always safe, touch-friendly flags. |
| [dubai-mortgage-calculator](https://github.com/artinbahmani/dubai-mortgage-calculator) | [open](https://artinbahmani.github.io/dubai-mortgage-calculator/) | Monthly payment plus every upfront fee of a Dubai purchase, visualized. |
| [crypto-ticker](https://github.com/artinbahmani/crypto-ticker) | [open](https://artinbahmani.github.io/crypto-ticker/) | Live top-20 prices, 7-day sparklines with hover inspection, pinnable coins. |

## How I work

I care about systems that keep running when nobody is watching. That means idempotent pipelines, dedup at every ingestion point, heartbeat monitors on every long-running process, alerting that reaches my phone, and backups that get restore-tested instead of just written to disk.

## Stack

**Languages:** Python, JavaScript / Node.js, SQL, Bash
**Data:** PostgreSQL (TimescaleDB, pgvector), Redis, Airtable
**Infra:** Docker Compose, Tailscale, Cloudflare, Uptime Kuma, self-hosted n8n
**Integrations:** Telegram Bot API, WhatsApp (Evolution API), exchange websockets (Bybit, Binance, Hyperliquid), LLM APIs in production
**Web:** Webflow, no-code front-ends wired to custom backends

## Now

Building a real-time trading intelligence platform: whale tracking on Hyperliquid, multi-timeframe market analysis, and a command-center dashboard, all running on my own local infrastructure.

📍 Dubai, UAE · 📫 artin.bahmani0@gmail.com
