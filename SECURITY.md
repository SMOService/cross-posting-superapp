# Security Policy

## Reporting a vulnerability

**Do not open a public GitHub issue.** Email **support@smoservice.media** with:

- A description of the issue and its impact
- Reproduction steps (a minimal proof of concept is ideal)
- Your suggested mitigation, if any

We'll acknowledge within **72 hours** and aim to land a fix or coordinated disclosure within **14 days** for confirmed issues. Researchers who disclose responsibly will be credited in the changelog (unless they prefer to remain anonymous).

## Scope

In scope:

- The Telegram bot **[@SuperappAIbot](https://t.me/SuperappAIbot)**
- The hosted Mini App at **content.smoservice.net**
- The credential storage and AES-256-GCM encryption
- The `initData` HMAC verification flow

Out of scope:

- Buffer / Upload-Post / Postmypost themselves (report upstream)
- Telegram Bot API itself (report to Telegram)
- Issues that require physical access to a user's Telegram session
