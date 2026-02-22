# skill-autonomous-orchestrator

An [Agent Skill](https://agentskills.io) for autonomous, continuous operation across a workspace.

## Overview

`skill-autonomous-orchestrator` is an autonomous meta-orchestrator that replaces the human in the loop of managing multiple concurrent agents. It continuously discovers work, dispatches agents, reviews results, and manages the full lifecycle across the user's workspace.

## Features

- **Continuous Work Discovery** — scans repositories, GitHub issues, pull requests, and package registries for improvements, security issues, and tasks.
- **Autonomous Dispatch** — spawns specialized agents for discovered tasks with clear acceptance criteria and context.
- **Intelligent Result Review** — applies the `user-proxy` skill's checklist to verify all work before acceptance, catching oversights and regressions.
- **Dynamic Monitoring** — tracks agent progress via non-blocking status checks and coordinates follow-up interactions.
- **User-First Interruptions** — stays responsive to direct user commands, prioritizing them over autonomous tasks.

## Installation

```bash
npx skills add metyatech/skill-autonomous-orchestrator --yes --global
```

## Development

This repository follows the standards defined in [AGENTS.md](./AGENTS.md).

### Scripts

- `npm run lint`: Run ESLint to check code quality.
- `npm run format`: Run Prettier to format the codebase.
- `npm run format -- --check`: Verify that files are correctly formatted.

### Project Structure

- `SKILL.md`: The skill definition and instructions (core logic).
- `AGENTS.md`: Repository-wide rules and engineering standards.
- `.github/workflows/ci.yml`: Continuous Integration pipeline.

## Related Skills

- [skill-user-proxy](https://github.com/metyatech/skill-user-proxy) — Review checklist used by the orchestrator.
- [skill-manager](https://github.com/metyatech/skill-manager) — Orchestration patterns and model selection.

## Security

Please refer to [SECURITY.md](./SECURITY.md) for reporting vulnerabilities.

## License

[MIT](./LICENSE)
