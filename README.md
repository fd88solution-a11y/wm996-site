# WM996 staging site

Static marketing pages for WM996, the Malaysia and Singapore online entertainment brand. This repository is a **staging preview** on GitHub Pages. It does not replace production.

## Preview

GitHub Pages serves the `main` branch from the site root (no custom domain):

**https://fd88solution-a11y.github.io/wm996-site/**

Paths shipped:

- `/` — home, including the only FAQ section and FAQPage JSON-LD
- `/promotion` — welcome offer, weekly rescue, VIP levels
- `/apps` — official iOS and Android install path
- `/slot` — classic reels, video slots, jackpots
- `/casino` — live baccarat, roulette, blackjack, dragon tiger
- `/sport` — football, basketball, tennis, esports
- `/blog` — registration guide
- `/affiliate` — revenue-share programme

To preview on your own machine, clone the repo and from its root run:

```bash
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.

## Staging rules

- Do not set a GitHub Pages custom domain. Leave `wm996.xyz` off this repository.
- Do not change production DNS, Cloudflare, or the live site at `https://wm996.xyz`.
- A cut from the current production site onto these files needs separate approval from the boss.
- Keep the Figma Make project that publishes today’s `wm996.xyz` site for at least 30 days. Do not delete that Make file when this preview goes up.
- Membership stays at `https://play.wm996.xyz`. This repo does not change that site or its footer.

## Search

Every HTML page includes `<meta name="robots" content="noindex,nofollow">` so the `*.github.io` preview is not indexed.

Each page’s canonical URL is `https://wm996.xyz` plus its path. Links between these pages are relative. The membership call to action is `https://play.wm996.xyz`.

`robots.txt` allows crawling and `sitemap.xml` lists the `https://wm996.xyz` URLs. Those two files are for a later, approved cutover. They do not move DNS.

On the day of an approved cutover, change the robots meta to `index,follow` before these files become what `wm996.xyz` serves. Leaving `noindex,nofollow` in place would hide production as well.

`.nojekyll` is present so GitHub Pages serves the files as written and does not run Jekyll.

## Assets

The Open Graph image is self-hosted at `assets/og.png`. The vector master is `assets/og.svg`. The image path in each page is relative, so the preview and a future production host both use the file in this repo. No `figma.site` URLs are used.
