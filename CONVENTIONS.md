# Vault conventions — RD Personal Management

This repo is the **git-backed second brain** (Obsidian-compatible). The Librarian agent writes here; every edit is a reversible git commit. Governance rule satisfied: the vault is git-backed, so Librarian edit access is **enabled**.

## Layout
- `Notes/` — one reference note per captured item (article / tweet / reel / page).
- `Tasks/Inbox.md` — actionable items captured from links, plain checkboxes.
- `Daily/` — (optional) daily logs / weekly summaries from other agents, routed via the Librarian.

## Reference notes
- Format: **`.qmd`** (Quarto markdown) — per the authoritative design spec; **user-confirmed 2026-07-02**. (Obsidian won't index `.qmd` natively; the tasks file stays `.md`. Switch is a one-line change if ever desired.)
- Filename: `Notes/YYYY-MM-DD-<slug>.qmd` (date = capture date).
- YAML frontmatter: `title`, `source` (URL), `captured` (date), `tags: [...]`, `kind: reference | actionable | both`.

## Actionable links
- Appended to `Tasks/Inbox.md` as: `- [ ] task (source-link 2026-07-02)`.
- A single link may produce **both** a reference note and a task (the Librarian decides, flags ambiguous to the Chief of Staff).

## Git
- Local working copy is the source of truth; `origin` (GitHub) backs it up and syncs devices.
- The Librarian commits each edit with a clear message. Push uses Git Credential Manager (GitHub auth required).
