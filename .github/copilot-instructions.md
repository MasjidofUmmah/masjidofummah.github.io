<!-- Short, focused guidance for AI coding agents working on this repo. -->
# Copilot / AI Agent Instructions

This repository is a small static website (GitHub Pages) composed of plain HTML and a single CSS file. There is no build tool, package manager, or tests. Make minimal, focused edits and prefer non-destructive changes.

- **Big picture:** A simple static site served from the repository root (username.github.io). Primary pages: `index.html`, `about.html`, `contact.html`, `donate.html`, `parking.html`, `prayer-times.html`. Styling lives in `styless.css` (note spelling).
- **Why this structure:** Pages are independent HTML files linked together with relative links; this keeps deployment simple (push to main and GitHub Pages serves root).

- **When editing:** Touch only the files required for the change. Preserve existing relative paths and file naming (particularly `styless.css`). If you rename `styless.css`, update every HTML file that references it and include a single commit describing the rename.

- **Local preview:** Use a simple static server to test changes.

  Example:

  - Run: `python3 -m http.server 8000` from the repo root and open `http://localhost:8000`.

- **Deployment note:** This repo appears to be `masjidofummah.github.io` (a user site). Changes pushed to the default branch (usually `main`) are published by GitHub Pages. If unsure, create a branch and open a PR rather than direct pushing.

- **Common patterns & examples:**
  - Navigation and relative links: update navigation links in `index.html` and mirrored copies on other pages. Keep relative linking style (e.g., `about.html`, `contact.html`).
  - CSS: `styless.css` is the single stylesheet. Search for that filename before changing. Example: update colors or font sizes here and verify across `index.html` and `prayer-times.html`.
  - Prayer times: `prayer-times.html` is likely static HTML. Do not attempt to add server-side logic; if dynamic behavior is required, propose a client-side JS file and document it in the PR.

- **Conventions & gotchas (from repo):**
  - File names are lowercase and use `.html` extension. Keep this style.
  - There is a misspelled stylesheet name: `styless.css`. Do not silently correct typos — treat renames as explicit, cross-file changes.

- **PR guidance for AI-generated changes:**
  - Create a focused branch like `fix/navbar-link` or `feat/prayer-times-update`.
  - Include a short PR description that lists modified files and rationale.
  - If you modify `styless.css` or rename it, include screenshots or a short list of pages checked (manual preview via `python3 -m http.server`).

- **What not to do:**
  - Do not introduce a build system, bundler, or dependencies in this repo without explicit instruction from the maintainers.
  - Do not convert site to a framework (React/Vue) in a single change.

- **Search targets for context:** Quick files to open when working on UI or content:
  - `index.html` — main landing
  - `prayer-times.html` — times content
  - `styless.css` — styling

If some behavior is unclear (e.g., deployment branch or intended update cadence), ask the maintainers before making sweeping changes.

---
Please review these instructions and tell me which parts need more detail or examples to be more actionable for contributors.
