# 🌐 Open WebUI Bangla

**A friendly Bangla web chat for your local AI — open it in the browser, talk in Bangla.**

## ✨ Features

- `docker-compose.bangla.yml` — runs on http://localhost:3000, wired to local Ollama, data in `./open-webui-data`.
- `bangla-prompts.json` — 3 starter prompts in Bangla: **বুঝিয়ে দাও** (explain), **চিঠি/আবেদন** (letter writing), **কোড ব্যাখ্যা** (explain code).
- Clean web interface — no terminal needed after the first start.

## 🚀 How to use

```bash
# 1. Start Ollama on this machine first (see ollama-bangla)
# 2. Start Open WebUI
docker compose -f docker-compose.bangla.yml up -d
```

Open http://localhost:3000, create the first admin account, pick your Ollama model (for example `bangla` from ollama-bangla), and paste a prompt from `bangla-prompts.json` to start.

## ⚠️ Honest limits

- The first account you create becomes the admin — keep its password safe.
- Needs Ollama running on the same machine for the free local path; otherwise add a provider key in Settings.
- The prompts are starters — they guide the model, they do not add new knowledge to it.

## 🇧🇩 বাংলা

**ওপেন ওয়েবইউআই বাংলা — ব্রাউজারে চলা বাংলা এআই চ্যাট।**

- ডকার দিয়ে এক কমান্ডে চালু হয় — http://localhost:3000
- ৩টা তৈরি বাংলা প্রম্পট: বুঝিয়ে দাও, চিঠি/আবেদন, কোড ব্যাখ্যা
- লোকাল Ollama মডেল দিয়ে চলে — ক্লাউড key ছাড়াই

## 📄 License

MIT — use it however you like.
