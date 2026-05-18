# Never Give Up Loop (パパボタン)

> *"Never give up. Live brightly. Until the end."*
> — Toshiya Mimura, Creator

A personal AI memory system that preserves your voice, memories, and values — so your family can keep talking to you, even after you're gone.

---

## What is this?

**Never Give Up Loop** is an open-source framework for building a personal AI that learns from your life data:

- 📷 **Photos** — 360,000+ images, auto-tagged by location, emotion, and subject
- 📧 **Emails** — Full-text search across decades of personal correspondence
- 🎵 **Music** — Your listening history, mood-matched and timeline-aware
- 🗣️ **Voice** — Your cloned voice, speaking in your own words
- 💬 **Conversation** — A chat interface your family can use to ask you anything

Built by a Japanese accounting professional with 20 years of experience, on a home NAS, for his children.

---

## Why?

Most people leave behind photos and documents.  
This system lets you leave behind **yourself**.

When you are gone, your children can ask:

- *"Dad, what were you thinking when you drove your S2000?"*
- *"What music did you love in your 30s?"*
- *"What did you always say about never giving up?"*

And the system answers — in your voice, from your memories.

---

## Architecture

```
Your NAS / Home Server
├── photo.db          # 360k+ photos, CLIP embeddings, GPS, emotion scores
├── mail.db           # Personal email archive, FTS5 full-text search
├── music.db          # Listening history, mood tags
├── voice/            # StyleBERT-VITS2 cloned voice model
└── FastAPI           # REST API for all services

Web Interface
├── /chat             # Talk to the AI persona
├── /timeline         # Browse life events by date
├── /monitor          # System health dashboard
└── /setup            # API key configuration wizard
```

---

## Requirements

- NAS or home server (Synology, QNAP, UGREEN, Raspberry Pi, etc.)
- Docker & Docker Compose
- GPU recommended (for voice synthesis)
- API keys: OpenAI / Anthropic Claude / Google Maps

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/toshiya-mimura/never-give-up-loop.git
cd never-give-up-loop

# Copy environment template
cp .env.template .env

# Start the system
docker-compose up -d

# Open setup wizard in your browser
open http://localhost:8000/setup
```

---

## Features

| Feature | Status |
|---|---|
| Photo search (semantic + keyword) | ✅ Ready |
| GPS reverse geocoding | ✅ Ready |
| Auto-tagging (31 categories) | ✅ Ready |
| Emotion scoring | ✅ Ready |
| Full-text email search | ✅ Ready |
| Music timeline | ✅ Ready |
| Voice cloning | ✅ Ready |
| AI chat persona | ✅ Ready |
| Vehicle photo search | ✅ Ready |
| System health monitor | 🔧 In progress |
| Docker one-click setup | 🔧 In progress |
| English UI | 🔧 In progress |
| FAQ Bot | 📋 Planned |

---

## Philosophy

This project was built on three beliefs:

1. **Never give up** — no matter what
2. **Live brightly** — find joy in every day
3. **Leave something behind** — not just photos, but your voice, your values, your self

The name *Never Give Up Loop* reflects the idea that your story doesn't end. It loops — continuing through the people you loved.

---

## About the Creator

**Toshiya Mimura** (三村俊也)  
Born 1963, Osaka, Japan.  
20 years in corporate accounting. Self-taught programmer.  
Built this system on a home NAS in 2026, for his daughter and son.

> *"I want my kids to be able to ask me anything, even after I'm gone."*

---

## License

MIT License — free to use, modify, and distribute.

---

## Contributing

Questions and ideas welcome via [GitHub Discussions](https://github.com/toshiya-mimura/never-give-up-loop/discussions).  
Bug reports via [GitHub Issues](https://github.com/toshiya-mimura/never-give-up-loop/issues).

---
## Background

This project was born from a personal story.

The creator wrote two semi-autobiographical works
that explain *why* this system exists:

- 📖 [コーラの王冠](https://note.com/ryojp3636/n/n2c96584190a4)
  *A semi-autobiographical novel. 14 chapters.*
- 📖 [40年後から来た男](https://note.com/ryojp3636/n/nbb3bb77b43e4)
  *An SF companion story.*

> *"I want my kids to be able to ask me anything,*
> *even after I'm gone."*


*Never Give Up Loop — because some conversations should never end.*
