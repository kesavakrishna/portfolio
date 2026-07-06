# Portfolio — Kesava Sai Krishna Kondepudi

Personal portfolio site. Single static HTML file, deployed on Vercel via GitHub integration (push to `main` = auto-deploy).

## Owner context

- AI Engineer at Bilvantis Technologies, Hyderabad, Mar 2024 – Jun 2026 (intern Mar–Jun 2024, then FTE "Programmer Analyst: AI"). Role has ended — site uses past tense for Bilvantis work.
- B.Tech in Electronics and Computer Engineering, Mahindra University, Hyderabad, 2020–2024 (mentioned in What's Next).
- Starting a full-time MS in Data Science at CU Boulder, Fall 2026. Career target: research engineering (reliability, interpretability). Site states he's looking for RA positions from Fall 2026.
- No Google Scholar profile yet (as of Jul 2026) — owner intends to create one; add the link to the Research section when he provides the URL.
- Contact on site: kesavakrishna91@gmail.com · github.com/kesavakrishna · linkedin.com/in/kesava-krishna. Phone number is deliberately NOT on the site (spam) — do not add it.

## Repo structure

- `index.html` — the homepage (HTML + CSS inline, no JS deps, no build step).
- `distribution-shift.html` — first entry in the Notes section: a RADEX post-mortem essay reusing the same design system. Same inline-CSS, zero-JS approach.
- `resume.pdf` — linked from the contact section via relative path `resume.pdf`. Keep this filename (lowercase — Vercel's host is case-sensitive) if replacing.
- `README.md` — one-liner for GitHub.
- `CLAUDE.md` — this file.

## Design system (do not drift from this without being asked)

Concept: "Noisy signals in, working systems out." The hero's signature element is an SVG waveform that starts as a noisy seismocardiogram and resolves into clean ECG beats — a direct reference to the owner's IEEE ICPEEV 2023 paper (SCG→ECG CycleGAN, 96.55% fidelity in extended work). Sections are labeled Signal 01–06.

- Colors (CSS vars in `:root`): paper `#F3F5F8`, ink `#101B2D`, muted `#56677D`, cobalt accent `#1F4FE0`, amber (metrics/highlights) `#D98A1F`, line `#D5DDE7`.
- Type: Archivo Black (display, uppercase headings), Source Serif 4 (body), IBM Plex Mono (labels/tags/metrics). Loaded from Google Fonts.
- Layout: max-width 1080px, 1px-line card grids, sticky nav. Responsive breakpoint at 860px. `prefers-reduced-motion` respected on the waveform animation — preserve this.
- Tone of copy: plain, specific, metric-driven. No buzzword filler. The recurring technical through-line is **distribution shift / reliability** — it appears in the hero, the RADEX card, and What's Next, and connects production work → research interests.

## Page sections (current)

1. Hero + waveform band, with role line (Bilvantis, Mar 2024 – Jun 2026)
2. Work (Signal 01) — 3 featured cards (Tiggo location intelligence, RADEX multi-tenant RAG, P2X migration platform) with amber metric lines, plus an "Also shipped" list (test automation, multi-agent BI, audio pipeline, secret scanner)
3. Research (Signal 02) — 2 publications with DOI links (IEEE ICPEEV 2023: doi.org/10.1109/ICPEEV58650.2023.10391941; J. Prediction Markets 2024: doi.org/10.5750/jpm.v18i1.2119)
4. Notes (Signal 03) — long-form writing; currently one entry linking to `distribution-shift.html`. When notes exceed ~3, that's the migration trigger from "Decisions" below (prefer Astro over Next.js).
5. Independent Projects (Signal 04) — Reflective AI Memory System, Corporate Risk Assessment (AutoGen), Crypto Sentiment Backtester — each links to its GitHub repo (reflective_ai, risk_analysis, buy_sell_pred). Card copy must honestly match what the linked repo actually contains.
6. What's Next (Signal 05) — CU Boulder MS, B.Tech line, focus areas (reliability under distribution shift, mechanistic interpretability, time series, geospatial AI)
7. Contact band (Signal 06, dark) + footer — includes RA-availability line

## Deployment

- Vercel project connected to this GitHub repo. Push to `main` deploys production; branches/PRs get preview URLs.
- No build command, no framework — output directory is the repo root. Keep it that way.

## Decisions already made (don't relitigate unless the owner asks)

- Stay a single static HTML file for now. Do NOT migrate to Next.js until there's a concrete trigger (e.g., a blog). Zero dependencies = zero maintenance during grad school.
- Custom domain planned (e.g., kesavakondepudi.com) — attach in Vercel settings when purchased.
- No photo on the site by choice.

## Likely next tasks

- Owner: review/sharpen `distribution-shift.html` sections 03–04 with real incident details (see REVIEW comment in that file), then push.
- Owner: create Google Scholar profile → add link to Research section.
- Owner: fix GitHub profile pins (should feature reflective_ai, risk_analysis, buy_sell_pred), add bio + website URL, improve reflective_ai README/description.
- Parked: OG/Twitter meta tags + og:image, favicon (confirmed 404 in prod), `scroll-padding-top`, "404 — Signal lost" page, JSON-LD Person schema.
- Custom domain purchase → attach in Vercel, then add canonical tag.
- Ongoing: add new publications/projects/notes as they happen; update location context after the Boulder move.