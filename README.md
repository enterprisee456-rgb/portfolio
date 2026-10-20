# Anderson Muriithi portfolio

A single static page (index.html). No build step, no dependencies.

## Deploy over the existing Vercel project (GitHub-connected)

1. Optional backup: in the repo, run `git checkout -b old-portfolio && git push -u origin old-portfolio`, then `git checkout main`.
2. Delete all the old files in the repo (src, package.json, vite/next config and so on).
3. Copy `index.html` and `vercel.json` from this folder into the repo root.
4. Commit and push. Vercel redeploys on its own.
5. Open https://enterprisee-portfolio-3g4m.vercel.app/ and check it.

If the build fails: Vercel project > Settings > Build and Development Settings.
Set Framework Preset to "Other" and clear any Build Command or Output Directory overrides.

## Deploy from your computer instead

Run `npx vercel --prod` inside this folder.

## What vercel.json does

- Tells Vercel this is a plain static site (no framework, no build).
- Adds security headers: Content-Security-Policy, X-Content-Type-Options, X-Frame-Options, Referrer-Policy and Permissions-Policy.

## Editing

Contact details, prices and text are all inside index.html. If you add scripts, images from other sites or embeds, update the Content-Security-Policy in vercel.json or the browser will block them.
