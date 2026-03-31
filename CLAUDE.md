# CLAUDE.md

This file documents the repository structure, development workflows, and conventions for AI assistants (Claude Code and others) working in this codebase.

---

## Repository Overview

**Project:** gamification-
**Repository:** [erdiantomy/gamification-](https://github.com/erdiantomy/gamification-)
**Status:** Early / initial stage — no source files committed yet.

This project is a gamification system. As code is added, update this file to reflect the actual structure, tech stack, and conventions in use.

---

## Repository Structure

```
gamification-/
├── CLAUDE.md          # This file
└── (project files to be added)
```

Update this tree as directories and files are introduced.

---

## Tech Stack

_To be determined as the project takes shape._ Common choices for gamification systems include:

- **Backend:** Node.js / Python / Go
- **Frontend:** React / Vue / plain HTML
- **Database:** PostgreSQL / MongoDB / Redis (for leaderboards/sessions)
- **Queue/Events:** Redis Streams / RabbitMQ / Kafka

Document the actual stack here once decided.

---

## Development Workflow

### Branching Strategy

- `main` — stable, production-ready code
- `dev` / `develop` — integration branch (if used)
- `feature/<short-description>` — feature branches
- `fix/<short-description>` — bug-fix branches
- `claude/<task-description>` — AI-assisted branches (auto-created by Claude Code)

### Getting Started

```bash
# Clone the repo
git clone https://github.com/erdiantomy/gamification-
cd gamification-

# Install dependencies (update command once stack is chosen)
# npm install  OR  pip install -r requirements.txt  OR  ...

# Run locally
# npm run dev  OR  python main.py  OR  ...
```

### Running Tests

```bash
# Update once test framework is chosen
# npm test
# pytest
# go test ./...
```

### Linting / Formatting

```bash
# Update once tooling is set up
# npm run lint
# ruff check .
# golangci-lint run
```

---

## Git Conventions

- **Commit messages:** Use the imperative mood, short subject line (≤72 chars). Examples:
  - `Add user points tracking module`
  - `Fix leaderboard ranking tie-break logic`
  - `Refactor badge award service`
- **No force-push to `main`.**
- **All commits on feature branches; merge via PR.**
- Commit messages automatically include a Claude Code session URL when commits are made by AI assistants.

---

## Code Conventions

Until the actual stack is established, these general conventions apply:

- Keep functions small and single-purpose.
- Validate all external inputs at system boundaries; trust internal interfaces.
- Do not add speculative abstractions or future-proofing code.
- Avoid commented-out dead code — delete it.
- Tests live alongside source or in a dedicated `tests/` directory (document when decided).

---

## AI Assistant Instructions

### Scope

- Only interact with the `erdiantomy/gamification-` repository.
- Develop on the branch specified in the task context (e.g., `claude/add-claude-documentation-eIwmQ`).
- Push with `git push -u origin <branch-name>`.
- Never push directly to `main` without explicit user permission.

### What to Update in This File

When adding significant new features or making architectural decisions, update CLAUDE.md to reflect:

1. Changes to the directory structure.
2. New dependencies or services added.
3. New test commands or lint rules.
4. Any domain-specific conventions (e.g., how points/badges are modeled).

### Dos and Don'ts

- **Do** read existing files before modifying them.
- **Do** keep changes minimal and focused on the task.
- **Do** run tests before committing.
- **Don't** add error handling for scenarios that can't happen.
- **Don't** create helpers for one-time operations.
- **Don't** add docstrings, comments, or type annotations to code you didn't change.
- **Don't** commit `.env` files, credentials, or large binaries.

---

## Key Domain Concepts

_(Update as the gamification model evolves.)_

| Concept | Description |
|---------|-------------|
| **Points** | Numeric value awarded to users for completing actions |
| **Badges** | Achievements unlocked when criteria are met |
| **Leaderboard** | Ranked list of users by points (global or scoped) |
| **Level** | User tier derived from accumulated points |
| **Quest / Challenge** | A set of actions that, when completed, yield a reward |

---

## CI / CD

_Not configured yet._ When CI is added (e.g., GitHub Actions), document:

- Workflow file locations (`.github/workflows/`)
- What triggers each workflow (push, PR, schedule)
- Required secrets/environment variables

---

## Environment Variables

_None yet._ Document all required environment variables here as they are introduced, e.g.:

| Variable | Required | Description |
|----------|----------|-------------|
| `DATABASE_URL` | Yes | PostgreSQL connection string |
| `REDIS_URL` | No | Redis URL for caching/leaderboards |
| `JWT_SECRET` | Yes | Secret for signing auth tokens |

---

*Last updated: 2026-03-31*
