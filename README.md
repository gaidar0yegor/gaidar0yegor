# yegor gaidar

I build things in Paris. The full stack — Go
distributed systems, Flutter mobile, on-device AI, blockchain, and
infrastructure. Eight years of shipping production code has taught me
the same lesson over and over: most systems are over-engineered, and
the second-best solution usually wins.

I work by constraint. AEON lives on 8 GB of RAM with zero cloud. The
cluster is nine Mac minis because compute you own beats compute you
rent. Crab-1 is a 1.7B model because the task didn't need
a bigger one. LobsterSwamp runs on my own iMac because I wanted
AI-agents-as-collaborators that answer to me, not to a SaaS.

## currently running

**the cluster** — a Nomad + Consul cluster spanning two Paris sites:
nine Mac minis (2011–2014), a PowerEdge T430, and Proxmox LXCs.
12 workers · 76 threads · 124 GB RAM, managed entirely by Ansible —
mutual TLS, ACLs, workload identity, Prometheus alerts that reach my
phone. The two sites started on colliding subnets, so everything
talks over a WireGuard mesh. The lessons became posts:
[a mac mini beats a xeon per core](https://yegorgaidar.org/blog/mac-mini-fleet-benchmark/) ·
[an address is an identity](https://yegorgaidar.org/blog/nomad-serf-address-identity/) ·
[alert rules that never fired](https://yegorgaidar.org/blog/alert-rules-that-never-fire/).

**ArchDogma** — started as a linter, became a catalog of engineering
failures caused by *following* the rules — the ones that quietly kill
projects. Segment's 140+ microservices, Basecamp's over-mocked test
suite. Twelve documented dogmas (eleven with postmortems) and a
Python CLI with function / module / git-history detectors that finds
them in your code. The catalog is the point. `pip install archdogma`
— v0.2.1 on [PyPI](https://pypi.org/project/archdogma/),
module-level import graph + coupling metrics on main.

**Crab-1** — a 1.7B tool-calling agent (Qwen3 + QLoRA) that profiles
French companies from open registries and the web. Trained on
synthetic episodes from its own pipeline; beats its base model on
every eval metric. The
recurring result: every sophistication I added — abstention,
multi-search — made it worse.
[Write-up](https://yegorgaidar.org/blog/small-model-simplicity-wins/).

**LobsterSwamp** — an autonomous agent swarm on my iMac. Voice notes
from Telegram → Paperclip control plane → Lobster (Claude Code) ships
code · Hermes triages on a local model. The swarm that actually does
my work while I drink coffee. Not a demo — it runs my days.

**AEON** — a self-evolving on-device AI companion. M1 · 8 GB RAM · zero
cloud. Phi-4 + MCTS + curiosity-driven learning + LoRA adaptation.

**[yegorgaidar.org](https://yegorgaidar.org)** — site + engineering
blog, 21 posts: distributed systems, on-device LLMs, architecture
fights at 3 AM.

## shipped in production

**QuackNet** — DePIN network-intelligence platform. Flutter iOS client +
Go backend. Users scan Wi-Fi networks, earn Solana tokens. Kafka ·
ClickHouse · PostgreSQL · Solana · H3 · Mapbox.

**Telegram Affiliate Publisher** — autonomous affiliate marketing bot.
Amazon PA API + OpenAI content + multi-language scheduling + Redis
caching. Running in production. Python · aiogram · PostgreSQL · Redis ·
Docker.

## stack

- **primary** — Go · Python · TypeScript · Dart
- **fluent** — Rust · Java · C / C++
- **systems** — Kafka · ClickHouse · PostgreSQL · Redis · Docker · distributed patterns
- **AI** — Claude (agent orchestration) · Ollama · MLX · QLoRA fine-tuning · Phi-4 · CoreML · MCTS · WebGPU
- **infra** — Proxmox · Nomad · Consul · Ansible · Prometheus · self-hosted LLM stacks · n8n · Netlify

## work with me

I take a few engagements alongside my own products:
[AI Sprint](https://yegorgaidar.org/ai-sprint.html) — your company on
private, self-hosted AI in 2 weeks · [architecture
audit](https://yegorgaidar.org/hire.html) — find what breaks before it
breaks · fractional SRE. GDPR-friendly, no cloud lock-in.

## where

paris · FR / EN / RU / UK · remote ok

## find me

[yegorgaidar.org](https://yegorgaidar.org) · [LinkedIn](https://linkedin.com/in/yegor-gaidar) · [@yegor_code](https://twitter.com/yegor_code)
