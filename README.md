# Open WebUI Bangla — বাংলায় লোকাল AI চ্যাট

Bangla-ready self-hosted Open WebUI setup, built on **open-webui/open-webui**.

- **Original repo:** https://github.com/open-webui/open-webui (user-friendly AI interface — supports Ollama, OpenAI API and more)

## কী আছে / What is inside

- `docker-compose.bangla.yml` — runs Open WebUI on http://localhost:3000, wired to local Ollama.
- `bangla-prompts.json` — 3 starter prompts in Bangla: বুঝিয়ে দাও (explain), চিঠি/আবেদন (letter writing), কোড ব্যাখ্যা (explain code).

## যা ঠিক করা হয়েছে / What was fixed

- Upstream's quickstart is a long `docker run` command that is easy to mistype. This turns it into a repeatable compose file using the exact image (`ghcr.io/open-webui/open-webui:main`), volume (`/app/backend/data`) and Ollama setting from the upstream README.
- Adds Bangla starter prompts — upstream ships with English-only examples.

## ব্যবহার / How to use

```bash
# 1. Start Ollama on this machine first (ollama-bangla)
# 2. Start Open WebUI
docker compose -f docker-compose.bangla.yml up -d
```

Open http://localhost:3000, create the first admin account, pick your Ollama model (e.g. `bangla` from ollama-bangla), and paste a prompt from `bangla-prompts.json` to start.
