# Decisions

Not published on the site (it lives at the repo root, outside `docs/`).

## 2026-10-04: Site generator is Zensical, deployed with GitHub Actions

**Decision:** Build the portfolio site with [Zensical](https://zensical.org), deployed to GitHub Pages by our own workflow (`.github/workflows/pages.yml`).

**Options considered**
- **just-the-docs on GitHub Pages** (Jekyll, branch deploy). No build workflow, but every page needs front matter (`title`, `nav_order`, layout), which shows as clutter on github.com. Dark mode needs hand-written toggle code. Looks plainer.
- **MkDocs Material.** Same look and config as Zensical, but concerns about MkDocs' long-term maintenance and the planned 2.0 rewrite.
- **Docusaurus.** More mature, but a React/Node app that is overbuilt for a handful of markdown pages.
- **Hugo.** Stable, but the most setup.

**Why Zensical**
- Nicer look, with dark/light toggle and search built in.
- Markdown files stay clean: no front matter. Navigation order lives in `mkdocs.yml`, so the files read well on github.com too.
- Built by the Material for MkDocs team and reads `mkdocs.yml`, so it can fall back to MkDocs Material if needed.

**Trade-offs accepted**
- We own the build: a GitHub Actions workflow is required (free for public repos; Pages must be set to "GitHub Actions" as the source).
- Zensical is pre-1.0 (0.0.67 when tested). The workflow installs the latest version on purpose; pin it in `pages.yml` if a release breaks the build.
- No strict mode yet (`--strict` is unsupported), so broken links will not fail the build. The lychee workflow is the safety net.
- Section pages live in `docs/`. The root `README.md` is the source for the home page: the build generates `docs/index.md` from it (stripping the `docs/` link prefix), and `docs/index.md` is gitignored. To preview locally, run the same `sed` command as in `pages.yml` first.

**Known quirks**
- Zensical ignores `exclude_docs`. Excluded files use the `exclude` plugin in `mkdocs.yml` instead (currently `CONVENTIONS.md`).
- Not yet verified: the deploy workflow on GitHub itself, and whether search still works with an explicit `plugins:` list.

**Alternatives not kept:** the just-the-docs (Jekyll, with a dark mode toggle) and MkDocs Material prototypes were built as throwaway worktrees and removed after this decision; neither was committed.
