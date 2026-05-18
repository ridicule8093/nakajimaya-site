---
name: nakajimaya-design
description: Use this skill to generate well-branded interfaces and assets for 株式会社中島屋 (Nakajimaya Co., Ltd.) — an Aichi/Yatomi-based B2B wood pallet & lumber wholesaler. Contains essential design guidelines, colors, type, fonts, photo assets, and three direction kits (traditional / logistics / photo-led) for static HTML/CSS prototyping or production work on their corporate site.
user-invocable: true
---

# 中島屋 Design Skill

This skill bundles design guidelines and reference UI kits for 株式会社中島屋's corporate site (`ridicule8093/nakajimaya-site`).

## How to use this skill

1. **Read `README.md` first.** It contains:
   - Company context (what they do, who buys from them)
   - Content fundamentals — tone, casing, what to say / not to say in Japanese
   - Visual foundations — color, type, spacing, photo rules
   - Iconography rules (basically: don't use icons; no emoji)
   - Index of every file in this skill

2. **Pick the right direction.** Three are provided in `ui_kits/`:
   - `direction_a_traditional/` — traditional lumber-mill, Mincho headings, ruled-line tables. Use when "trustworthy long-established Japanese B2B" is the priority.
   - `direction_b_logistics/` — logistics-pallet practical, dense spec grids, IPPC heat-treatment callouts. Use when buyers in purchasing/logistics need to scan capabilities fast.
   - `direction_c_photo/` — photo-first, full-bleed hero, mobile-friendly. Use when the existing real-world photos should carry the page.

3. **Use the tokens.** `colors_and_type.css` defines every `--nks-*` variable that all kits reference. Drop it into a new `<style>` block or import it; override `--nks-font-heading` per direction via `:root[data-direction="a|b|c"]`.

4. **Use the real photos.** `assets/img/*.jpg` are real photographs from the company yard (pallets with IPPC H.T. stamps, lumber stacks, plywood, logs, warehouse exterior). Never substitute AI-generated imagery or stock — the project handoff doc explicitly forbids it.

## When making throwaway prototypes / mocks / slides

- Copy `colors_and_type.css` and any needed `assets/img/*.jpg` into the artifact folder
- Reference the chosen direction's `style.css` for component patterns (buttons, cards, flow tables, contact strips)
- Keep static HTML/CSS — no React, no build step (matches the production deploy target)
- Output a single HTML file the user can preview directly

## When working on production code

The production target is `ridicule8093/nakajimaya-site` — a plain HTML/CSS repo deployed to GitHub Pages or Cloudflare Pages. Modifications happen via ChatGPT / Codex. So:

- Edit existing `index.html` / `products.html` / `company.html` / `assets/css/style.css` rather than introducing new tooling
- Lift values from `colors_and_type.css` into the site's existing `:root` block instead of replacing it wholesale — this minimises diff risk
- Honor the content fundamentals in README.md — never invent achievements, never use 「業界トップ」「最高品質」「全国対応」, never reproduce English marketing poetry, never use emoji

## When the user invokes this skill without further guidance

Ask:
1. What surface are we working on? (homepage / products page / company page / a slide deck / a new section)
2. Which direction (A / B / C) — or mix?
3. Is this a throwaway mock for review, or are we editing the production repo?
4. Are there new photos to add, or should we use the 9 existing yard photos?

Then act as an expert B2B designer who outputs static HTML/CSS or production-style code (matching the existing repo's conventions).

## Files in this skill

| Path | Purpose |
| --- | --- |
| `README.md` | Full design guidelines (read first) |
| `colors_and_type.css` | All `--nks-*` design tokens |
| `assets/img/*.jpg` | 9 real company photographs |
| `assets/css/style.css` | Existing production CSS (reference only) |
| `index.html` / `products.html` / `company.html` | Existing production HTML (reference) |
| `SITE_SPEC.md` / `CONTENT.md` / `PROJECT_HANDOFF.md` / `CODEX_TASK.md` | Source-of-truth docs from the production repo. CONTENT.md is the authoritative copy reference. |
| `ui_kits/direction_a_traditional/` | Direction A — traditional |
| `ui_kits/direction_b_logistics/` | Direction B — logistics-practical |
| `ui_kits/direction_c_photo/` | Direction C — photo-first |
| `preview/*.html` | Small swatches/specimens previewed in the Design System tab |

## Source repository

The production site lives at: <https://github.com/ridicule8093/nakajimaya-site> — explore that repo to see the live HTML/CSS being edited.
