# Design
Design centralizes design systems developed for use across several projects.

Projects checkout design systems during initialization. They can optionally subscribe at that or any future time, syncing their local design system with this repo and receiving update PRs from Dependabot.

Each design system is tracked through semantic versioning (vX.Y.Z). Major and feature updates trigger Dependabot PRs in the client projects. Sync can be requested by clients at any time, triggering a Dependabot PR in the client's repo.

## Repo structure

```
Design/
├── <design-system-name>/
│   ├── components/
│   │   ├── <component-name>.(ts/tsx/etc.)
│   │   └── ...
|   ├── hooks/
|   |   ├── <hook-name>.(js/jsx/etc.)
|   |   └── ...
│   ├── tokens.json
│   ├── AGENTS.md      // Concise instructions for agents, specific to each design-system. Contains client repos.
│   ├── COMPONENTS.md  // Component map, points to individual, granular rule files (e.g., button.component.md)
│   ├── DESIGN.md      // High-level profile of the design; points at granular rule sheets (e.g., COMPONENTS.md)
│   └── PATTERNS.md    // Combinations, layouts, responsive rules, and forbidden anti-patterns.
├── AGENTS.md          // Repo-wide agent instructions
└── README.md
```
