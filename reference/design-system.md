# Design system

Rules the generated page must keep. The template already encodes them; preserve them when
you adapt it. Do not invent new CSS, only swap the vibe tokens, fonts, and content.

## Look and material
- Dark glass is the signature. Surfaces (avatar, product tiles, link rows, socials) are
  translucent: a faint fill + 1px border + `inset 0 1px 0` top highlight + `backdrop-filter`.
  Keep all three; that inner edge is what makes glass read as glass.
- One gradient accent per page (`--a1` to `--a2`), used only on the CTA background, the product
  thumbnails, and the icon tint. Everything else is glass or solid text.
- OKLCH only. Never `#000`/`#fff`. The vibes in `reference/vibes.md` handle the palette.

## Motion (Emil Kowalski curves, already in the template)
- Animate `transform` and `opacity` only. Easing `--ease-expo` for enter and settle.
- Entrance is a staggered fade-up (`.rise`, `--i` index, 60ms steps). When you add or remove
  blocks, renumber `--i` sequentially from 0 so the cascade stays in order.
- Press feedback: `transform: scale(0.98)` on `:active`.
- All `:hover` effects are gated behind `@media (hover: hover) and (pointer: fine)` so touch
  devices do not need two taps. Keep that wrapper.
- Honor `prefers-reduced-motion` (movement off, opacity kept). Already handled.

## Accessibility (WCAG 2.2 AA, non-negotiable)
- Exactly one `<h1>` (the page name). Section labels are `<h2>`.
- The initials avatar is decorative, so it stays `aria-hidden="true"`. If you use an image
  avatar instead, give it a real `alt` (the page name) and delete the initials version.
- Every icon-only control has an `aria-label`; every decorative icon has `aria-hidden="true"`.
- Visible focus: the `:focus-visible` outline stays.
- Touch targets stay large: link rows are full-width, socials are 50px, the avatar is 84px.
- Contrast: the vibes are tuned so dark text on the gradient clears 4.5:1 on both ends, light
  text sits on dark glass, and `--mute` clears 4.5:1 on `--bg`. If you hand-pick a gradient,
  keep `--a1`/`--a2` light (L ~0.7 to 0.85) and `--mute` near L 0.68.
- Never rely on color alone; rows keep a text label, a leading icon, and a chevron.
- Keep `lang` and `prefers-color-scheme`/`prefers-reduced-motion` handling.

## Do not
- No gradient TEXT (`background-clip: text`). The gradient is for backgrounds only; text is a
  single solid color. Hierarchy comes from size and weight.
- No dead `href="#"`. If a URL is unknown, omit that link or ask for it.
- No em dashes (use commas, periods, parentheses). No filler words ("elevate", "seamless",
  "unleash"). Concrete and short. Keep the bio to one line.

## Icons (Tabler webfont via CDN, `<i class="ti ti-NAME">`)
- Outline names only (no `-filled`). Brand icons are `ti-brand-NAME`: `instagram`, `tiktok`,
  `youtube`, `x`, `linkedin`, `github`, `spotify`, `dribbble`, `behance`, `facebook`,
  `threads`, `pinterest`, `twitch`, `discord`, `whatsapp`.
- Match icons to meaning. CTA: `calendar-event` (book), `sparkles`/`wand` (work with me),
  `shopping-bag` (shop), `mail` (subscribe/contact), `ticket` (events), `coffee` (tip).
  Row/product icons: pick the closest concept (`layout-grid`, `player-play`, `mail`, `movie`,
  `box`, `download`, `book`, `map-pin`, `device-laptop`).

## Final gate (check before delivering)
1. One `<h1>`, `<h2>` section labels, avatar `aria-hidden` (or `alt` if an image).
2. Every icon-only link has an `aria-label`; decorative icons `aria-hidden`.
3. No `href="#"` left; every link is real or removed.
4. `--i` indices are sequential with no gaps.
5. One vibe applied to the `VIBE TOKENS` block; `theme-color` and fonts set to match.
6. No gradient text. Reduced-motion, hover-gating, and focus styles intact.
