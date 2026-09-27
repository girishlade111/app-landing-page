# App Landing Page

A modern **marketing landing page for a notes/productivity app**, generated with [v0](https://v0.app) and built on Next.js. It covers the classic SaaS landing structure — header nav, hero with CTA, feature highlights, pricing/testimonial sections — and is fully static, so it can be dropped onto any static host as-is.

## Sections

- Header with nav links ("Start Here", "Products", "Solutions", "Compare", "Pricing", "FAQs") + "View Plans" CTA
- Hero: "New — Make your notes great again" badge, headline "A notes app that works like an Organizer", dual CTA buttons
- Feature/testimonial and pricing sections (extendable — see `app/page.tsx`)

## Tech stack

- **Next.js 15.2.4** (App Router)
- **React 19**
- **Tailwind CSS 3.4** + tailwindcss-animate
- **shadcn/ui** (Radix primitives, cva, clsx, tailwind-merge)
- **Lucide icons**
- TypeScript

## Quick start

Requires Node.js 18+.

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Build & static export

Fully client-side (no API routes, no server actions) → static export:

```bash
npm run build          # writes static files to ./out
```

Serve `./out` with any static host (Cloudflare Pages, Netlify, GitHub Pages, `npx serve out`).

## Project structure

```
app-landing-page/
├── app/
│   ├── layout.tsx        # Root layout (fonts, metadata)
│   ├── page.tsx          # Entire landing page (sections)
│   └── globals.css
├── components/
│   ├── theme-provider.tsx
│   └── ui/button.tsx     # shadcn button
├── components.json
├── lib/utils.ts          # cn() helper
├── public/               # Images (incl. professional-headshot.png)
├── styles/globals.css    # Legacy duplicate of app/globals.css
├── next.config.mjs       # images.unoptimized, output: 'export'
├── tailwind.config.ts
└── postcss.config.mjs
```

## Customizing

- Replace `LOGO`, the headline, and nav labels in `app/page.tsx`.
- Swap `public/professional-headshot.png` with real imagery.
- Update `app/layout.tsx` metadata (title, description) for SEO.

## Environment variables

None. No backend.

## Deployment

Static — works on any static host. Repo ships with `output: 'export'` so `npm run build` writes to `./out` directly.

---

Built by Girish Lade — [ladestack.in](https://ladestack.in)
