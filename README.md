# airlineschat

SubX room #18 — Airline issue-resolution. Delays, bags, refunds — not official support. (preview).

Static site. `siteId` is `airlineschat`. Custom domain in `CNAME` is `airlineschat.com`. Preview banner and `noindex` stay on.

Deploy `main` from `/` on GitHub Pages (Cloudflare DNS next). Factory shell talks to Firebase project `subx-skins` (fetches `firebase-web-config.json`; no API keys in this repo).

## Outside this repo

- Firestore allowlist for `siteId` `airlineschat` (CTO).
- Cloudflare zone + NS flip for `airlineschat.com` (CTO).
