# Gaming Projects Workspace

Central workspace (`C:\Users\maxtr\Desktop\projects`) for organizing and maintaining structured gaming notes, progression milestones, and Jekyll ([Just the Docs](https://just-the-docs.com)) documentation repositories.

Each game project lives in its own independent `gaming_notes_<game>` Git repository, while this root workspace repository tracks shared agent instructions, workspace conventions, and reusable project prompts.

## Active Gaming Projects

| Project | Game | Notes & Docs | Agent Guide | GitHub Pages Target |
| :--- | :--- | :--- | :--- | :--- |
| [`gaming_notes_total_war_warhammer_3`](./gaming_notes_total_war_warhammer_3/) | [Total War: Warhammer III](https://store.steampowered.com/app/1142710/Total_War_WARHAMMER_III/) | [`README.md`](./gaming_notes_total_war_warhammer_3/README.md) · [`docs/`](./gaming_notes_total_war_warhammer_3/docs/index.md) | [`AGENTS.md`](./gaming_notes_total_war_warhammer_3/AGENTS.md) | `https://mooikos.github.io/gaming_notes_total_war_warhammer_3` |
| [`gaming_notes_lootun`](./gaming_notes_lootun/) | [Lootun](https://store.steampowered.com/app/1960270/Lootun/) | [`README.md`](./gaming_notes_lootun/README.md) · [`docs/`](./gaming_notes_lootun/docs/index.md) | [`AGENTS.md`](./gaming_notes_lootun/AGENTS.md) | `https://mooikos.github.io/gaming_notes_lootun` |

## Reusable Agent Prompts

### 1. Bootstrap a New Gaming Project (from Workspace Root)

```text
I want to start on a new gaming project for the game "<GAME_NAME>".
Please create a new folder "gaming_notes_<game_slug>", initialize a separate Git repository inside it, research authoritative info about the game, and set up:
- README.md + AGENTS.md tailored to the game
- Jekyll + Just the Docs scaffold in docs/ (including milestones and core game sections)
Please also keep the root workspace README.md and AGENTS.md up-to-date and commit changes cleanly in their respective Git repositories.
```

### 2. Iteratively Build Milestones & Gaming Notes (inside a Project)

```text
Please help me recursively create and expand gaming notes documents for "<GAME_NAME>" in gaming_notes_<game_slug> by asking focused questions step by step.
In particular, help me organize:
1. Short-term, mid-term, and long-term gaming milestones
2. Everything I discover and want to document in-game (builds, mechanics, items, strategies, and progression logs)
Always keep all index pages, Jekyll frontmatter, cross-links, and AGENTS.md up-to-date.
```

## Multi-Repository Layout

- **Root Workspace Repo** (`.`): Tracks workspace-level [`README.md`](./README.md), [`AGENTS.md`](./AGENTS.md), and [`.gitignore`](./.gitignore) (ignoring `.ssh/`, `git/`, and `gaming_notes_*/`).
- **Project Repos** (`gaming_notes_<game>/`): Independent Git repositories on branch `main`, each ready to preview locally (`cd docs && bundle exec jekyll serve`) and publish via GitHub Pages.
