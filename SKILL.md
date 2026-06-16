---
name: biolink-studio
description: Use when someone wants to create a link-in-bio, linktree, bio link, link page, or "links" landing page for a person, brand, creator, or business. Triggers on requests to build, generate, or make a bio link / link hub / social links page, or an Instagram/TikTok "link in bio".
license: MIT
---

# biolink-studio

Generate a single self-contained, accessible, animated link-in-bio page (one `index.html`)
in a dark glass aesthetic. Interview the user first, then assemble their page from the audited
template. Never invent the user's content; ask for it.

## Workflow

### 1. Interview (always first, never skip)
Ask in small batches, adapt to the answers, and do not assume. Cover:

- **Identity** — page or business name; a one-line bio (what they do); initials for the avatar
  (1 to 3 letters) OR an avatar image URL; page language (default English).
- **Primary action** — the single most important button, if any (book a call, work with me,
  shop, subscribe, contact, tip). Need its label and URL.
- **Links** — the main list. For each: a title, an optional one-line sub-label, and a URL.
- **Products** (optional) — for each: name, price, URL (any checkout).
- **Socials** (optional) — which platforms and their URLs.
- **Footer** (optional) — a homepage link or credit.
- **Design** — pick a vibe (gradient) from `reference/vibes.md`: Aurora, Spectrum, Mint,
  Sunset, Ocean, Mono. Suggest one based on their business and confirm. Offer a custom gradient
  if they have brand colors.

Then play back a short summary and confirm before generating.

### 2. Assemble
Start from `assets/template.html` and adapt it (read `reference/design-system.md` first):
1. Apply the chosen vibe from `reference/vibes.md`: replace the whole `VIBE TOKENS` block and
   set `theme-color`. Swap the Google Fonts `<link>` only if the vibe changes the fonts.
2. Fill identity. Use the initials avatar (keep it `aria-hidden`) OR the avatar `<img>` with a
   real `alt` (delete the other). The name is the `<h1>`.
3. Build content: keep, duplicate, or delete the CTA, PRODUCTS, LINKS, and SOCIALS blocks to
   match their answers. Renumber every `--i` sequentially from 0. Choose a fitting Tabler icon
   for the CTA, each product thumbnail, and each link row (see design-system for names).
4. Fill the `<title>`, meta description, and OG tags. Add the favicon/OG image if given.

### 3. Deliver
- Write to `./index.html` (or ask where).
- Preview it if you can (open in a browser or a static server) and show the result.
- Tell them how to host it free: drag the file onto Netlify Drop, push to a GitHub repo with
  Pages enabled, or deploy with Vercel. It is one file with no build step.

## Hard rules
Follow `reference/design-system.md` exactly. Most important:
- Keep accessibility intact: one `<h1>`, `<h2>` labels, `aria-label` on icon-only controls,
  `aria-hidden` on decorative icons, focus styles, large targets, reduced-motion, hover-gating.
- Glass + one gradient accent is the whole look. No gradient text (backgrounds only).
- Never ship a dead `href="#"`; omit unknown links. No em dashes. No filler words.

## Quality gate (run before handing it over)
Use the final checklist in `reference/design-system.md`: one h1, h2 labels, avatar aria,
icon-only aria-labels, no `#` links, sequential `--i`, vibe + theme-color + fonts set, no
gradient text, reduced-motion/hover/focus intact.

## Files
- `assets/template.html` — the complete base page to adapt.
- `reference/vibes.md` — six dark gradient presets, all contrast-checked.
- `reference/design-system.md` — material, motion, accessibility, and copy rules.
- `examples/` — a finished sample page for reference.
