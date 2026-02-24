# AGENTS.md

Guidance for AI coding agents working in this repository.

## Project overview
- `index.html`: Main single-page netRadio UI and client-side logic.
- `deploy.sh`: Generates `server.js`, writes a Dockerfile, builds image, and runs container.
- `README.md`: User-facing project and run documentation.

## Working agreements
- Keep this project lightweight: prefer plain HTML/CSS/JS unless a dependency is clearly justified.
- Avoid large refactors unless requested. Favor small, focused edits.
- If you change user-facing behavior, update `README.md` accordingly.
- Do not commit generated artifacts like `server.js` or local temporary files.

## Validation checklist
When making non-trivial changes, run at least:
```bash
git status --short
```
If runtime logic changes, also validate by serving `index.html` or running:
```bash
./deploy.sh 3000
```
(only where Docker is available).

## Commit and PR style
- Use clear, scoped commit messages (e.g., `docs: ...`, `feat: ...`, `fix: ...`).
- Summarize what changed and why in the PR body.
- Mention any limitations or skipped checks explicitly.
