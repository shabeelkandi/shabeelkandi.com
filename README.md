# shabeelkandi.com

Personal workspace. The home page is a list of projects by date; each project is one page under `public/`.

## Add a project

1. Create `public/<slug>/index.html`.
2. Add a row to the list in `public/index.html` (date and title).
3. Deploy.

## Deploy

```bash
npx wrangler deploy
```

Hosted on Cloudflare Workers static assets, free plan.

## Custom domain (one-time)

The domain is registered at Namecheap. To serve the site at shabeelkandi.com:

1. Cloudflare dashboard → Add a domain → `shabeelkandi.com` → Free plan. Cloudflare shows two nameservers.
2. Namecheap → Domain List → shabeelkandi.com → Nameservers → Custom DNS → paste those two nameservers.
3. Once Cloudflare marks the zone Active, add this to `wrangler.jsonc` and deploy:

```jsonc
"routes": [
  { "pattern": "shabeelkandi.com", "custom_domain": true },
  { "pattern": "www.shabeelkandi.com", "custom_domain": true }
],
```
