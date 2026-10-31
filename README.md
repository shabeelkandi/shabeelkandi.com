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
