# airlineschat

SubX room #18: Airline issue-resolution. Delays, bags, refunds: not official support. (live).

Static site. `siteId` is `airlineschat`. Custom domain in `CNAME` is `airlineschat.com`. Live: preview banner removed, search indexing allowed (`robots.txt` + `sitemap.xml`).

Deploy `main` from `/` on GitHub Pages (Cloudflare DNS next). Factory shell talks to Firebase project `subx-skins` (fetches `firebase-web-config.json`; no API keys in this repo).

## Nest URLs

GitHub Pages answers `/<slug>` from a generated `<slug>.html` stub (200) instead of the `404.html` bounce. Stubs cover every nest in `site.json`. User-created nests (`users.userNests` in Firestore) are not in that catalog and still use the bounce.

Re-run after editing `site.json` nests:

```
python3 nest_stubs.py .
```

## Outside this repo

- Firestore allowlist for `siteId` `airlineschat` (CTO).
- Cloudflare zone + NS flip for `airlineschat.com` (CTO).
