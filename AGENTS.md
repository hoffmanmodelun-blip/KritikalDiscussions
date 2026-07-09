# AGENTS.md — Kritikal Discussions website

Rules for any AI agent working in this repository. Follow them exactly.

## The site

- `index.html` is the entire live website (kritikaldiscussions.com). Single file: HTML, CSS, and JS together.
- It uses a JavaScript in-page router (`go(name)`) that swaps `<section class="page" id="page-*">` elements, plus scroll-reveal animations.
- Non-technical co-founders also edit this site through a visual editor (`(ALL) - Kritikal-Editor - FINAL.html`) that publishes commits directly to `main`. **Assume `main` can move at any time, even between your commands.**

## Git rules — never break these

- Work on the `main` branch **only**. Never create a branch, pull request, fork, or worktree.
- **Never** run `git push --force`, `--force-with-lease`, `git reset --hard`, or `git rebase`.
- **Never** use `--allow-unrelated-histories`.
- **Never** delete or rename `index.html`.
- If a `pull` or `push` is rejected, conflicts, or reports divergent/unrelated histories: **STOP immediately, show the exact output, and wait for instructions.** Do not attempt to resolve it.

## Standard workflow

1. `git pull origin main` — always, before making any edit.
2. Make the requested change.
3. Stage, commit with a clear message, `git push origin main`.
4. Confirm the push succeeded.

Keep the window between pull and push as short as possible; a co-founder may publish at any moment.

## Editing conventions

- Preserve the router, the scroll-reveal animation classes (`reveal`, `in`, `d1`–`d6`), and the CSS custom properties in the `:root` block. Do not restructure or reformat the file.
- Do not split `index.html` into multiple files, and do not extract the CSS or JS.
- Photos are either files in the image folders (`Founder Images/`, `Camp 2026/`, `Kritikal Project/`, `Main Page/`) or base64 data URIs embedded directly in `index.html`. Both are valid — do not "clean up" data URIs into files, or vice versa.
- Image folder names contain spaces and capital letters. Match them exactly; GitHub Pages is case-sensitive.
- `CNAME` maps the custom domain. Never modify or delete it.

## Scope

- Make the minimal change requested. Do not refactor, reformat, "optimize," or touch unrelated sections.
- If a request seems to require breaking a rule above, stop and ask.
