# mopajazz.com

Personal portfolio — Astro static site, deployed on Vercel.

## Run locally
    npm install
    npm run dev        # http://localhost:4321

## Deploy
Push to GitHub → import in Vercel. Framework preset: Astro. No config needed.
Point mopajazz.com at the Vercel project when ready.

## Where things live
- `src/content/work/*.md` — case studies. **To add one: drop in a markdown
  file with frontmatter (title, summary, order, tools, link, featured).
  That's the whole job.** No layout code, no HTML.
- `src/content/lab/*.md` — Lab entries. Frontmatter only; body optional.
- `src/content/config.ts` — the schemas. Add a field here (e.g. `year`),
  and every entry can use it.
- `src/styles/global.css` — all design tokens in `:root`. One place.
- `src/layouts/Base.astro` — nav, footer, fonts.
- `src/pages/` — one file per route. `work/[...slug].astro` builds every
  case study page from the collection automatically.

## Adding a Maps page later
1. Add a `maps` collection to `src/content/config.ts`
2. Drop images in `public/maps/`
3. Create `src/pages/maps/index.astro` (copy lab/index.astro as a start)
4. Add `{ href: '/maps/', label: 'Maps' }` to the nav array in Base.astro

## Open items
- Component library preview link (Lab entry + ACA-122 study)
- MKT-120 sample module Vercel link (case study artifact row)
- Deploy prompt-engineering + ACC-121 Rise exports, add links to Lab entries
