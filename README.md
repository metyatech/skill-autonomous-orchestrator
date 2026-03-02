# skill-autonomous-orchestrator

An [Agent Skill](https://agentskills.io) for autonomous, continuous operation across a workspace.

## What it does

Replaces the human in the loop of managing multiple concurrent agents. The orchestrator continuously:

- **Discovers work** — scans repos, GitHub, and package registries for improvements, issues, and tasks
- **Dispatches agents** — spawns agents with self-contained prompts, manages conflict avoidance
- **Reviews results** — applies user-proxy checklist to catch oversights before accepting work
- **Handles follow-ups** — interacts with agents via follow-up messages, retries failures
- **Stays responsive** — the user can interrupt at any time with priority tasks

## When it triggers

- User wants hands-off autonomous operation
- User says "run continuously", "take over", "auto-pilot"

## Installation

```bash
npx skills add metyatech/skill-autonomous-orchestrator --yes --global
```

## Development

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS recommended)
- [npm](https://www.npmjs.com/)

### Setup

```bash
npm install
```

### Commands

- `npm run format` — Format all files with Prettier
- `npm run format:check` — Check formatting with Prettier
- `npm run compose` — Regenerate `AGENTS.md` from the rules source
- `npm run verify` — Run all verification checks (formatting, composition)

## Related skills

- [skill-user-proxy](https://github.com/metyatech/skill-user-proxy) — Review checklist used by the orchestrator
- [skill-manager](https://github.com/metyatech/skill-manager) — Single-task orchestration (the orchestrator uses the same dispatch patterns)

## License

MIT
