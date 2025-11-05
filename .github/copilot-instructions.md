# Copilot / AI agent instructions — slds3

Purpose
- Help an AI coding agent be immediately productive in this repository: a small static site served from XAMPP's htdocs.

Quick snapshot
- Repo root entry: `index.html` (located at `/Applications/XAMPP/xamppfiles/htdocs/slds/slds3/index.html`).
- This project is a plain/static web directory. There is no build system, package.json, or test harness present.

How to run / preview locally
- This site is served by XAMPP/Apache under the `htdocs` tree. To preview, ensure Apache is running and open:
  - http://localhost/slds/slds3/
- Common XAMPP control: use the XAMPP control panel on macOS, or run the bundled script (if available):
  - `/Applications/XAMPP/xamppfiles/xampp start` and `/Applications/XAMPP/xamppfiles/xampp stop` (use with sudo if needed).

Where to edit
- Edit `index.html` directly for page content. Add static assets (CSS/JS/images) as sibling files or subfolders and reference them with relative paths, e.g. `./css/styles.css`.

Conventions and patterns discovered here
- No framework conventions: prefer small, self-contained changes. Keep markup and static assets colocated for this simple site.
- When adding PHP back-end pages, place them in this same directory and rely on Apache to execute `.php` files.

Debugging hints
- Use the browser DevTools (Console/Network) for front-end errors.
- Apache logs (if something server-side fails) are at `/Applications/XAMPP/xamppfiles/logs/error_log` and `access_log`.

Development notes for AI agents
- Don't invent missing build tools or package managers; check for `package.json`, `composer.json`, `Makefile` first — none are present.
- Keep edits minimal and localized (single file changes preferred). If adding many files, update README.md with usage and link paths.
- Use relative URLs for assets. Absolute-system paths (e.g., `/Applications/...`) should not be committed — use repository-relative paths instead.

Examples (how to add an asset)
- Add `css/styles.css` and reference in `index.html` like:
  - `<link rel="stylesheet" href="css/styles.css">`

Merge strategy
- If a `.github/copilot-instructions.md` already exists, preserve any existing detailed steps and only append/replace factual environment-specific items (paths, run commands, logs). Here no existing file was found, so this is the initial guidance.

Questions for the human maintainer
- Do you expect this folder to remain a static site, or should agents scaffold a frontend toolchain (npm, bundler) when adding interactive features?
- Any preferred commit/PR rules (linters, formatting) to encode here?

If anything in this file is unclear or missing, tell me what you'd like added and I'll update it.
