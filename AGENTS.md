# AGENTS.md — Gaming Projects Workspace

## Workspace Overview
This workspace (`C:\Users\maxtr\Desktop\projects`) organizes and maintains gaming-related documentation projects and progression notes.
Each game project lives in its own `gaming_notes_<game>` folder and independent Git repository with its own project-specific `AGENTS.md`:

- **[`gaming_notes_total_war_warhammer_3`](./gaming_notes_total_war_warhammer_3/AGENTS.md)** — Structured notes, item databases, race guides, and Tabletop Caps army compositions for *Total War: Warhammer III*.
- **[`gaming_notes_lootun`](./gaming_notes_lootun/AGENTS.md)** — Progression milestones, class/Ascendancy builds, base/profession mechanics, crafting, and raid notes for *Lootun*.

## Core Principle: Always Keep Everything Up-to-Date
- **Always keep all files, links, indexes, and documentation up-to-date** whenever creating, editing, renaming, or removing files inside any project or at the workspace root.
- Keep both this root [`AGENTS.md`](./AGENTS.md), root [`README.md`](./README.md), and each project's `AGENTS.md` / `README.md` / `docs/index.md` synchronized whenever projects, conventions, or structures change.

## Multi-Repository Git Conventions
- **Independent Repositories**:
  - The root workspace (`C:\Users\maxtr\Desktop\projects`) is its own Git repository tracking workspace-level documentation (`.gitignore`, `AGENTS.md`, `README.md`).
  - Root `.gitignore` explicitly excludes `.ssh/`, `git/`, and `gaming_notes_*/` so credentials, portable binaries, and child repositories are never nested or leaked.
  - Each `gaming_notes_<game>` folder is a standalone Git repository (`main` branch) so it can be versioned and deployed independently to GitHub Pages (`https://mooikos.github.io/gaming_notes_<game>`).
- **Clean Commits**: Always run Git commands with `-C <repo-path>` (or inside the target repository) so changes are committed to the proper repository.

## Standard Project Architecture (`gaming_notes_<game>`)
- **Documentation Site**: Jekyll + [Just the Docs](https://just-the-docs.com) served from `docs/` (`_config.yml`, `Gemfile`, `Gemfile.lock`, `index.md`, and `kebab-case` section folders).
- **Interactive Note-Taking**: Support iterative Q&A workflows to organize **short / mid / long-term gaming milestones** alongside structured game mechanics, builds, items, and progression findings.

## Local Environment (Windows Portable Setup)
- **Portable Git**: `C:\Users\maxtr\Desktop\projects\git\cmd\git.exe` (added to User `PATH`)
- **SSH Keys & Known Hosts**: `C:\Users\maxtr\Desktop\projects\.ssh\id_ed25519` (configured in `git/etc/gitconfig`)
- **Git Author**: `Massimiliano De Vivo <5393529+mooikos@users.noreply.github.com>`
