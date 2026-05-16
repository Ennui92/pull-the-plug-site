# pull-the-plug-site

Promo + waitlist landing page for the game **Pull the Plug**.

Hosted on GitHub Pages at <https://ennui92.github.io/pull-the-plug/>.

The waitlist form posts to the [`ermis-waitlist`](https://github.com/Ennui92/ermis-dev/tree/main/workers/waitlist) Cloudflare Worker. Same anti-spam stack as the comments box on ermis.dev: honeypot, form-age gate, per-IP rate limit, Turnstile captcha. Emails are sha256-hashed before they touch storage.

Devlog lives on <https://ermis.dev/posts/>.

## Deploy

This repo deploys via GitHub Pages on every push to `main`. Nothing else to do.

## Local preview

Open `index.html` in a browser. The waitlist will post to the live worker (CORS allowlist already includes `ennui92.github.io` and `localhost` variants).
