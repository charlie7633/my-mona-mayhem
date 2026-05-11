# GitHub Copilot - Repository Instructions

This file helps future Copilot sessions understand and work with this repository.

## Build, test, and lint commands
- Start dev server: `npm run dev` (runs `astro dev`).
- Build production: `npm run build` (runs `astro build`).
- Preview build: `npm run preview` (runs `astro preview`).
- Astro CLI: `npm run astro` -> `astro`.

Notes: package.json contains no `test` or `lint` scripts in this template. Add test/lint scripts to package.json if you add a test runner or linter.

## High-level architecture
- Framework: Astro v5. The project is configured for server output using the `@astrojs/node` adapter (see `astro.config.mjs` -> `output: 'server'`, `adapter: node({ mode: 'standalone' })`).
- Runtime: Node.js (see README for recommended Node versions depending on workflow).
- Pages and site content live under `src/` (notably `src/pages/`). Static assets are in `public/`.
- Workshop & docs: interactive workshop content and localized guides are in `workshop/` and `docs/` (localized subfolders for `es` and `pt_BR`).
- API surface: the app uses GitHub contribution graph data (workshop exercises add API routes/pages as needed).

## Key conventions and patterns
- Dual workshop tracks: `VS Code` track (editor-first) vs `CLI` track (Copilot CLI). When using Copilot sessions, mention which track and the workshop step/path (e.g., `workshop/03-agent-mode.md`).
- Localization: localized README/workshop content exists (e.g., `README.es.md`, `README.pt_BR.md`, `workshop/es` etc.). Keep changes to localized content in parallel files.
- Server build: `astro.config.mjs` targets `server` output with Node standalone adapter  expect a Node server build artifact when running `npm run build`.
- Minimal template: this repo is a workshop starter; many features (tests, linters, CI) are intentionally absent.

## Files & assistant-config checks performed
Searched for common AI assistant config files and existing Copilot instructions; none were found in the repository root (no `CLAUDE.md`, `.cursorrules`, `AGENTS.md`, `.windsurfrules`, `.clinerules`, or existing `copilot-instructions.md`).

## Where to start in a Copilot session
- Run `npm install` then `npm run dev` to boot the site locally.
- If following the workshop, open `workshop/00-overview.md` (or localized path) and reference the specific step file to provide precise, scoped instructions to Copilot.
- When proposing code edits, reference file paths (e.g., `src/pages/index.astro`) and the workshop step to keep changes scoped.

---

If you'd like, add project-specific test and lint commands to `package.json` and I can update these instructions to include single-test invocation examples (e.g., `npx vitest path/to/test`).
