# Alex Fialko — Full-Stack & AI Engineer

**TypeScript · React · Next.js · Node.js · Python · AI integrations**
📍 Prague, Czech Republic · Remote (CET) · 🟢 Open to roles & contracts

---

## About

I build products end-to-end — from requirements and architecture through to production
deployment. Frontend on React and Next.js, backend on Node.js or Python, AI integrations
on top of LLM APIs, deployment on Vercel and Railway.

Most of my commercial work sits in three areas: Telegram automation, AI-integrated
dashboards, and data extraction platforms. I've also owned the non-code side — writing
technical specs, scoping and pricing projects, and running client communication directly.

## Tech Stack

**Frontend:** React · Next.js · TypeScript · JavaScript · Vite · Tailwind · HTML5/CSS3
**Backend:** Python · Node.js · Express · FastAPI · Fastify · aiogram · grammY · REST · WebSocket · JWT
**Data & queues:** PostgreSQL · pgvector · SQLite · Redis · BullMQ · ARQ · Prisma · Alembic
**AI:** Anthropic Claude · OpenAI API · Google Gemini · structured outputs · RAG · MCP servers
**Tools & Deploy:** Docker · Docker Compose · Vercel · Railway · GitHub Actions · Tailscale · Git

## Featured Projects

- **[Remote Jobs Hub](https://github.com/MERSEI/remote-jobs-hub)** — vacancy aggregator over
  Telegram channels. Six services in one compose file: an MTProto collector reading whitelisted
  sources only, a rule-based prefilter that drops noise *before* any LLM call, structured-output
  extraction into normalized fields, and two-layer dedup (exact + semantic via pgvector). Ships
  to users as a Telegram Mini App with HMAC-verified `initData` auth.
  `Python · FastAPI · Telethon · ARQ · PostgreSQL/pgvector · Next.js`

- **[LeadRadar](https://github.com/MERSEI/LeadRadar)** — Threads lead pipeline: headless
  scraping, Gemini relevance scoring, Telegram delivery. Two BullMQ queues on Redis sit between
  the stages, so a Playwright crash doesn't lose scraped posts and a transient 429 doesn't kill
  the run. Scores are cached by `sha256(post text)` — the same post seen under several keywords
  costs a Redis `GET`, not a second billed call. `TypeScript · BullMQ · Redis · Playwright · Gemini`

- **[antiTCK](https://github.com/MERSEI/antiTCK)** — anonymous incident-report bot with mandatory
  human moderation. Every submission is sanitized before publishing — phone numbers, emails,
  @usernames, URLs, licence plates — and coordinates are rounded to district level. There is no
  auto-publish path in the codebase; that's an invariant, not a setting.
  `Node.js 22 · TypeScript · grammY · Prisma · PostgreSQL · Vitest`

- **[crypto-widget](https://github.com/MERSEI/crypto-widget)** — resident desktop widget: a
  docked pill that expands into a live Binance watchlist with charts and spike alerts. Native
  window behaviour (always-on-top, docking) handled in Rust, because the web layer can't express it.
  `Tauri 2 · React 19 · Rust`

- **[TON Testnet Wallet](https://github.com/MERSEI/Ton-testnet)** — self-custodial TON wallet,
  Telegram-style UI, live updates over WebSocket. Shipped, then audited: 25 fixes across key
  handling, input validation and balance-refresh races, with the suite going 78 → 347 tests.
  `TypeScript · React · Vite · WebSocket · Vitest`

- **[Wallet Analytics Dashboard](https://dashboard-bice-rho-61.vercel.app)** — transactions,
  token flows and balance history for any Ethereum address on the Etherscan V2 API. A later audit
  closed a publicly reachable withdraw endpoint and took tests from 0 to 175.
  `Next.js · TypeScript · Vitest`

- **[Data Room MVP](https://acme-data-rooms.vercel.app)** — due-diligence document room:
  nested folders, PDF upload and preview, instant search, IndexedDB persistence, no backend.
  `React 19 · TypeScript · Zustand · Vitest`

- **[AI Integrator — Landing](https://ai-integrator-landing.vercel.app)** — bilingual
  marketing site with 10 live Gemini-backed tools, two-tier Upstash rate limiting and validated
  email capture. Tools that need scraping unavailable from serverless are labelled as demos
  rather than faked. `Next.js 15 · TypeScript · Tailwind · Framer Motion`

### Selected private work

- **Agent Farm** — hub-and-spoke agent platform: Telegram gateway, Fastify orchestrator, and
  per-VPS RAG workers. Workspace isolation is enforced by Postgres RLS (`SET LOCAL
  app.workspace_id`), not by application code; the only public surface is one webhook, everything
  else listens on a Tailscale mesh, and the model never gets a shell tool.
  `TypeScript · Fastify · BullMQ · PostgreSQL RLS · Docker · Tailscale`

- **Chronicles** — a text game where the dice are rolled by code, never by the model: the LLM
  names a skill and difficulty *before* the roll and narrates a result it didn't decide. The
  deterministic engine has zero dependencies and zero API calls, so balance is debugged for free —
  500 stubbed runs caught four defects, including one where succeeding at checks made a skilled
  player die sooner than a random one. `TypeScript · Anthropic API · Vitest`

More in the repository list: an
[AI IDE with a RAG pipeline and NATS-orchestrated agents](https://github.com/MERSEI/Vibe),
an [Instagram content-intelligence bot](https://github.com/MERSEI/Tr-Dev) (Whisper + OCR + LLM
function calling), and several production Telegram bots.

## Experience

**Team Lead / Full-Stack Developer** · Freelance · 2023–2024
Led 4 developers on commercial Telegram bots — code review, architecture decisions,
client communication. Shipped production bots with auth, payments and admin panels.

**Full-Stack Developer** · Freelance · 2022–Present
Web apps, dashboards and automation for paying clients. End-to-end delivery from spec
to deploy.

## How I work with AI

I use Claude and Copilot for boilerplate and for moving through unfamiliar APIs.
Architecture, review and debugging stay with me. Pick any repository here and I'll walk
you through why it's built that way and what I'd change — that's the part worth judging.

## Contact

- 📧 aleksfialko15@gmail.com
- 💼 LinkedIn: [Alex Fialko](https://www.linkedin.com/in/alex-fialko-2a0275356)
- 🌐 Portfolio: [portfolio-chi-sepia-jfbw53mb9i.vercel.app](https://portfolio-chi-sepia-jfbw53mb9i.vercel.app)
- 🕐 CET · 🗣 EN fluent · RU/UA native · CZ basic

*Open to remote Full-Stack / AI engineering roles and contract projects.*
