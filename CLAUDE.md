# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

Static marketing site for Rise Financial Wellness. No build step, no package.json, no framework — just HTML files that load Tailwind and Nunito from CDNs. Serve locally with `python -m http.server 8000` or `npx serve .`, or open the HTML directly.

## Files

- `index.html` — landing page with three-way audience toggle (Members / Institutions / Community).
- `about.html` — mission, values, team, impact.
- `name-research.html` — standalone internal artifact for the ongoing rebrand effort (see recent commits: "name-research: Round 3 shortlist", etc.). Dark-themed, independent styling — do not treat its conventions as canonical for the marketing pages.
- `logo.png` — the only binary asset.

## Architecture notes that aren't obvious from one file

**Tailwind config is inlined per HTML file.** Each page redeclares the same `tailwind.config` block with the Rise palette and Nunito. If you add a brand token or font weight, update every page that uses it — there is no shared config file.

**Brand tokens (keep in sync across pages):**
- `rise-blue` `#364463` · `rise-brown` `#a37d64` · `rise-orange` `#e4905c` · `rise-gold` `#eac351` · `rise-cream` `#ece6e1` · `rise-slate` `#3c454b`
- Font: Nunito (400/600/700/800). Buttons use `rounded-2xl`.

**Audience toggle pattern (`index.html`).** `setAudience(audience)` in the inline `<script>` at the bottom is the only interactivity. It shows/hides DOM nodes by id convention: for each audience in `['members', 'institutions', 'community']` it toggles `hero-{audience}` and `features-{audience}` plus the matching `toggle-{audience}` / `mobile-toggle-{audience}` buttons. When adding audience-specific sections, follow this id naming or the toggle won't pick them up. Adding a fourth audience means updating the array in the script, adding both desktop and mobile buttons, and adding the matching `hero-*` / `features-*` sections.

**Placeholder graphics are tracked in `README.md`.** The "Placeholder Graphics Needed" section enumerates every image spec (dimensions, style). When swapping in real assets, cross-check that list rather than inferring from the current DOM.
