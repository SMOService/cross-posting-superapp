# Cross-Posting Superapp

> One Telegram bot. All your socials. Forward a message — it lands on X, LinkedIn, Threads, Instagram, TikTok, Reels, Shorts, VK, OK, Дзен — routed through your Buffer, Upload-Post and Postmypost accounts.

**🌐 Landing page:** **[content.smoservice.net](https://content.smoservice.net)**
**🤖 Telegram bot:** **[@SuperappAIbot](https://t.me/SuperappAIbot)**
**📖 Russian:** [README.ru.md](README.ru.md)

This repository hosts the product page, brand assets and documentation for Cross-Posting Superapp. The product itself is a hosted Telegram Mini App + bot — you don't self-host it.

---

## What it does

```
forward in Telegram  →  pick a project (1 tap)  →  fan-out
                                                    ├──► Buffer    → X / LinkedIn / Threads / FB / IG / ...
                                                    ├──► Upload-Post → TikTok / Reels / Shorts / VK Clips
                                                    └──► Postmypost → VK / OK / Дзен / Threads / IG
```

You bring your own Buffer / Upload-Post / Postmypost API keys. The bot orchestrates fan-out — your provider accounts hold the OAuth with each social network.

---

## Why this exists

If you run more than one brand — a business, a personal account, a content creator you manage — you've felt this pain:

- Buffer covers text+image well but not short-form video.
- Upload-Post covers TikTok / Reels / Shorts well, but it's a separate dashboard.
- Postmypost covers RU socials (VK / OK / Дзен) that Western aggregators skip.

**No single aggregator covers everything.** Building yet another aggregator from scratch takes months. Cross-Posting Superapp is the missing **router** in front of the three that together cover ~every network, organised by **projects** so the same bot serves your business, your personal feed, and your client's account without leaking keys between them.

---

## Features

### Multiple projects, one bot
"My business", "Personal", "Client X" — each project keeps its own provider keys, its own channel selection, its own routing rules. Switch between projects with one tap.

### TEXT vs VIDEO routing
Some networks live for text. Others live for short-form vertical video. Each project decides per-mode where its posts go — so when you forward a 30-second TikTok-style video, it doesn't get awkwardly posted as a video link on LinkedIn.

### Forward is the workflow
No upload forms. No scheduling UIs to learn. Forward a Telegram message — bot detects the media type, asks which project, fans out. Two taps to publish across 10+ networks.

### Telegram Stars billing
Pay in Stars right inside Telegram. No credit cards. No cross-border payment friction. Cancel any time, your projects stay forever.

### Encrypted-at-rest credentials
Your Buffer / Upload-Post / Postmypost API keys are AES-256-GCM encrypted with a per-deployment key. The bot only ever holds plaintext in memory during a fan-out call — never on disk, never in logs.

---

## Pricing

| Tier         | Price          | Projects     |
|--------------|----------------|--------------|
| Free         | Free           | 1            |
| Standard     | 490⭐ / month  | up to 5      |
| Unlimited    | 980⭐ / month  | ∞            |
| Project slot | 100⭐ one-time | +1 permanent |

Pay through Telegram Stars — no card details ever touch us.

---

## Get started

1. Open **[@SuperappAIbot](https://t.me/SuperappAIbot)** in Telegram → `/start`
2. Tap **Open Mini App** → create your first project
3. Paste your Buffer / Upload-Post / Postmypost API keys (we encrypt them on receipt)
4. Pick which channels you want this project to publish to per mode (TEXT / VIDEO)
5. Forward a post from any Telegram chat into the bot — done

---

## Brand assets

Brand assets and screenshots live in [`/img`](./img). Free to use for press, integration partners, or self-built reviews.

---

## Ecosystem

Superapp is the **distribution** layer. These sibling Telegram bots cover the rest of running a channel — create the content, fetch media, move it between channels:

- **[@ZavodClawbot](https://t.me/ZavodClawbot)** — AI Content Factory: pick sources → AI writes original on-brand posts and publishes them on a schedule
- **[@TonChatAIbot](https://t.me/TonChatAIbot)** — AI assistant for text, images and ideas ([tonchat.ai](https://tonchat.ai))
- **[@SaveVideoProbot](https://t.me/SaveVideoProbot)** — download videos from TikTok / YouTube / Reels / VK for your posts
- **[@BridgePostBot](https://t.me/BridgePostBot)** — copy & AI-translate posts between Telegram channels

Open-source building blocks:

- **[Buffer Poster Bot](https://github.com/SMOService/buffer-poster-bot)** — self-hostable single-user predecessor (open source, MIT)
- **[Cross-Post Bridge AI bot](https://github.com/SMOService/Cross-Post-Bridge-AI-bot)** — AI-powered TG-to-TG channel bridge with rewriting and translation

---

## Support & contact

- Issues, feature requests, integration questions → [open an issue](https://github.com/SMOService/cross-posting-superapp/issues/new)
- Security disclosures → [SECURITY.md](SECURITY.md)
- General contact → **support@smoservice.media**

---

## License

This repository (docs + brand assets) is [MIT](LICENSE). The product itself is a hosted commercial service operated by SMOService.
