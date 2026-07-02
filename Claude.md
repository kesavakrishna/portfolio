# Portfolio — Kesava Sai Krishna Kondepudi

Personal portfolio site. Single static HTML file, deployed on Vercel via GitHub integration (push to `main` = auto-deploy).

## Owner context

- AI Engineer at Bilvantis Technologies, Hyderabad (production LLM systems).
- Starting a full-time MS in Data Science at CU Boulder, Fall 2026. Career target: research engineering (reliability, interpretability).
- Contact on site: kesavakrishna91@gmail.com · github.com/kesavakrishna · linkedin.com/in/kesava-krishna. Phone number is deliberately NOT on the site (spam) — do not add it.

## Repo structure

- `index.html` — the entire site (HTML + CSS inline, no JS deps, no build step).
- `resume.pdf` — linked from the contact section via relative path `resume.pdf`. Keep this filename if replacing.
- `CLAUDE.md` — this file.

## Design system (do not drift from this without being asked)

Concept: "Noisy signals in, working systems out." The hero's signature element is an SVG waveform that starts as a noisy seismocardiogram and resolves into clean ECG beats — a direct reference to the owner's IEEE ICPEEV 2023 paper (SCG→ECG CycleGAN, 96.55% fidelity in extended work). Sections are labeled Signal 01–05.

- Colors (CSS vars in `:root`): paper `#F3F5F8`, ink `#101B2D`, muted `#56677D`, cobalt accent `#1F4FE0`, amber (metrics/highlights) `#D98A1F`, line `#D5DDE7`.
- Type: Archivo Black (display, uppercase headings), Source Serif 4 (body), IBM Plex Mono (labels/tags/metrics). Loaded from Google Fonts.
- Layout: max-width 1080px, 1px-line card grids, sticky nav. Responsive breakpoint at 860px. `prefers-reduced-motion` respected on the waveform animation — preserve this.
- Tone of copy: plain, specific, metric-driven. No buzzword filler. The recurring technical through-line is **distribution shift / reliability** — it appears in the hero, the RADEX card, and What's Next, and connects production work → research interests.

## Page sections (current)

1. Hero + waveform band
2. Work — 3 featured cards (Tiggo location intelligence, RADEX multi-tenant RAG, P2X migration platform) with amber metric lines, plus an "Also shipped" list (test automation, multi-agent BI, audio pipeline, secret scanner)
3. Research — 2 publications with DOI links (IEEE ICPEEV 2023: doi.org/10.1109/ICPEEV58650.2023.10391941; J. Prediction Markets 2024: doi.org/10.5750/jpm.v18i1.2119)
4. Independent Projects — Reflective AI Memory System, Corporate Risk Assessment (AutoGen), Crypto Analysis Engine
5. What's Next — CU Boulder MS, focus areas (time series, geospatial AI, mechanistic interpretability)
6. Contact band (dark) + footer

## Deployment

- Vercel project connected to this GitHub repo. Push to `main` deploys production; branches/PRs get preview URLs.
- No build command, no framework — output directory is the repo root. Keep it that way.

## Decisions already made (don't relitigate unless the owner asks)

- Stay a single static HTML file for now. Do NOT migrate to Next.js until there's a concrete trigger (e.g., a blog). Zero dependencies = zero maintenance during grad school.
- Custom domain planned (e.g., kesavakondepudi.com) — attach in Vercel settings when purchased.
- No photo on the site by choice.

## Likely next tasks

- git init, first commit, push to GitHub, connect to Vercel (if not done yet).
- Add one-line README.md for the repo.
- Pin + write READMEs for the Reflective Memory System and risk-assessment repos on GitHub (the site links there prominently).
- Ongoing: add new publications/projects as they happen; update location context after the Boulder move.