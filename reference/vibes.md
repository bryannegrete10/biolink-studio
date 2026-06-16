# Vibes

Each vibe is a dark glass theme with a gradient accent (used on the CTA, the product
thumbnails, and the icon tint). All are OKLCH and WCAG AA verified: light text on dark glass,
dark text on the gradient, `--mute` clears 4.5:1. To apply one, replace the whole
`VIBE TOKENS` block in `assets/template.html` with the vibe's block and set the `theme-color`.
Fonts stay Space Grotesk (display) + Geist (body) unless you want to vary them.

Pick by feeling, or let the user choose. Default is **Aurora**.

| Vibe | Gradient | Good for |
|------|----------|----------|
| Aurora | cyan to violet | default, tech, creative, agencies |
| Spectrum | violet to magenta | music, nightlife, fashion, events |
| Mint | teal to emerald | wellness, finance, productivity, eco |
| Sunset | amber to coral | food, travel, lifestyle, photography |
| Ocean | blue to cyan | dev tools, SaaS, science, sport |
| Mono | silver to slate | minimal, luxury, editorial, b2b |

---

## Aurora (default)
theme-color `#0e1016`
```css
--bg: oklch(0.13 0.02 265); --ink: oklch(0.98 0.005 250); --ink-soft: oklch(0.88 0.012 250); --mute: oklch(0.68 0.02 258); --glass: oklch(1 0 0 / 0.06); --glass-soft: oklch(1 0 0 / 0.04); --brd: oklch(1 0 0 / 0.12); --hi: oklch(1 0 0 / 0.14); --a1: oklch(0.83 0.12 200); --a2: oklch(0.7 0.16 292); --on-accent: oklch(0.16 0.03 265); --glow: oklch(0.7 0.15 250 / 0.5); --bloom-1: oklch(0.7 0.15 200 / 0.5); --bloom-2: oklch(0.6 0.18 295 / 0.5); --bloom-3: oklch(0.6 0.16 255 / 0.4);
```

## Spectrum
theme-color `#15101a`
```css
--bg: oklch(0.14 0.025 320); --ink: oklch(0.98 0.005 320); --ink-soft: oklch(0.88 0.012 320); --mute: oklch(0.69 0.025 322); --glass: oklch(1 0 0 / 0.06); --glass-soft: oklch(1 0 0 / 0.04); --brd: oklch(1 0 0 / 0.12); --hi: oklch(1 0 0 / 0.14); --a1: oklch(0.74 0.15 300); --a2: oklch(0.72 0.17 350); --on-accent: oklch(0.16 0.03 330); --glow: oklch(0.68 0.18 330 / 0.5); --bloom-1: oklch(0.62 0.19 305 / 0.5); --bloom-2: oklch(0.62 0.18 352 / 0.5); --bloom-3: oklch(0.58 0.16 280 / 0.4);
```

## Mint
theme-color `#0d1513`
```css
--bg: oklch(0.14 0.02 175); --ink: oklch(0.98 0.005 175); --ink-soft: oklch(0.88 0.012 175); --mute: oklch(0.69 0.025 172); --glass: oklch(1 0 0 / 0.06); --glass-soft: oklch(1 0 0 / 0.04); --brd: oklch(1 0 0 / 0.12); --hi: oklch(1 0 0 / 0.14); --a1: oklch(0.85 0.12 178); --a2: oklch(0.76 0.15 150); --on-accent: oklch(0.16 0.03 175); --glow: oklch(0.74 0.14 165 / 0.5); --bloom-1: oklch(0.72 0.14 180 / 0.5); --bloom-2: oklch(0.66 0.16 150 / 0.45); --bloom-3: oklch(0.6 0.13 200 / 0.4);
```

## Sunset
theme-color `#16100c`
```css
--bg: oklch(0.14 0.02 40); --ink: oklch(0.98 0.006 60); --ink-soft: oklch(0.88 0.012 50); --mute: oklch(0.69 0.03 45); --glass: oklch(1 0 0 / 0.06); --glass-soft: oklch(1 0 0 / 0.04); --brd: oklch(1 0 0 / 0.12); --hi: oklch(1 0 0 / 0.14); --a1: oklch(0.85 0.13 75); --a2: oklch(0.72 0.16 30); --on-accent: oklch(0.18 0.03 40); --glow: oklch(0.74 0.15 50 / 0.5); --bloom-1: oklch(0.74 0.15 70 / 0.5); --bloom-2: oklch(0.64 0.17 28 / 0.5); --bloom-3: oklch(0.6 0.14 350 / 0.38);
```

## Ocean
theme-color `#0c1118`
```css
--bg: oklch(0.13 0.02 245); --ink: oklch(0.98 0.005 240); --ink-soft: oklch(0.88 0.012 240); --mute: oklch(0.68 0.022 244); --glass: oklch(1 0 0 / 0.06); --glass-soft: oklch(1 0 0 / 0.04); --brd: oklch(1 0 0 / 0.12); --hi: oklch(1 0 0 / 0.14); --a1: oklch(0.8 0.12 232); --a2: oklch(0.82 0.13 200); --on-accent: oklch(0.16 0.03 245); --glow: oklch(0.7 0.14 220 / 0.5); --bloom-1: oklch(0.66 0.15 235 / 0.5); --bloom-2: oklch(0.7 0.14 200 / 0.45); --bloom-3: oklch(0.58 0.14 260 / 0.4);
```

## Mono
theme-color `#14151a`
```css
--bg: oklch(0.15 0.006 260); --ink: oklch(0.98 0.003 260); --ink-soft: oklch(0.86 0.006 260); --mute: oklch(0.68 0.01 260); --glass: oklch(1 0 0 / 0.06); --glass-soft: oklch(1 0 0 / 0.04); --brd: oklch(1 0 0 / 0.12); --hi: oklch(1 0 0 / 0.13); --a1: oklch(0.84 0.015 260); --a2: oklch(0.72 0.02 260); --on-accent: oklch(0.18 0.01 260); --glow: oklch(0.7 0.02 260 / 0.4); --bloom-1: oklch(0.6 0.03 250 / 0.34); --bloom-2: oklch(0.55 0.03 280 / 0.32); --bloom-3: oklch(0.5 0.02 240 / 0.3);
```

## Custom accent
To make your own, copy any block and change `--a1` / `--a2` (the gradient) and the three
`--bloom-*` hues. Keep `--a1` and `--a2` light (L around 0.7 to 0.85) so the dark CTA text
stays readable, and keep `--mute` near L 0.68 so it clears 4.5:1 on the dark `--bg`.
