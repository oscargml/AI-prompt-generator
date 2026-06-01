# OmniPrompt — Free Private AI Prompt Generator

A free, open-source, **strictly client-side** AI prompt generator. Build clean,
structured XML prompts for ChatGPT, Claude, and Gemini — with automatic PII
masking, token estimates, a prompt quality score, quick-start templates, and
shareable deep links. No backend, no accounts, **zero data logging**.

**Live:** https://oscargml.github.io/AI-prompt-generator/

## Features

- **Structured prompt compiler** — outputs `<role>`, `<context>`, `<task>`,
  `<constraints>`, and `<json_schema>` tags that frontier models parse reliably.
- **Auto PII masking** — redacts emails, IPs, and phone numbers before the
  prompt reaches your clipboard (toggle on/off).
- **Dynamic `{{variables}}`** — detected automatically; fill values in once.
- **Quick-start templates** — Code Reviewer, Blog Writer, Data Analyst, JSON
  Extractor, ELI5.
- **Prompt quality score** — live 0–100 meter rewarding a complete prompt.
- **Token estimator** — color-coded safe / warn / danger.
- **Shareable deep links** — `#p=…` encodes the full prompt state in the URL.
- **Daily build streak** — local, private, `localStorage`-based gamification.
- **100% client-side** — nothing is sent anywhere.

## Tech stack

- Single static `index.html` — vanilla JS, no build step.
- Tailwind CSS via CDN.
- Buy Me a Coffee widget for optional support.
- Google Analytics (gtag) + Google Search Console verification.

## File layout

| File | Purpose |
|------|---------|
| `index.html` | The entire app (markup, styles, logic). |
| `favicon.svg`, `apple-touch-icon.png`, `og-image.png`, `logo.png` | Brand assets. |
| `google25f1072709fa8a10.html` | Search Console verification token. |

## Local development

```bash
python -m http.server 8099
# open http://localhost:8099/index.html
```

## Monetization & SEO setup

Wired and live:
- **Donations** — Buy Me a Coffee (`velmorpub`): floating widget + support section.
- **SEO** — canonical, Open Graph, Twitter Card, JSON-LD (`WebApplication` +
  `FAQPage`), keywords, real 1200×630 OG image.
- **Analytics** — GA4 `G-MMPSM1H3E4`; Search Console verified.

Needs one manual step to activate:
- **Google AdSense** — replace `ca-pub-XXXXXXXXXXXXXXXX` in `index.html`
  (the `ADSENSE_CLIENT` constant **and** the loader `<script src>` in `<head>`)
  with your real publisher ID, then enable **Auto Ads** at AdSense → Ads → By
  site. Ad units stay dormant until a valid ID is set, so nothing looks broken
  before approval. Remove the `.ad-slot` "Advertisement" placeholder CSS once
  ads serve.

## License

Open source. Built for secure, local AI engineering.
