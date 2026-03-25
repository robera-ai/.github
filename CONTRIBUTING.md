# Contributing to Robera.AI

Thank you for contributing. This guide covers the conventions we follow across all repositories.

## Stack

- **TypeScript** — all code, end-to-end
- **Bun** — runtime, package manager, test runner
- **Turborepo** — monorepo orchestration
- **Vitest** — unit testing
- **Playwright** — E2E testing (where applicable)

## Branch Naming

All branches must use a category prefix:

```
feat/   — new feature
fix/    — bug fix
chore/  — maintenance, dependencies, config
docs/   — documentation only
```

Examples: `feat/order-execution-engine`, `fix/websocket-reconnect`, `chore/bump-bun`.

## Commit Messages

We use [Conventional Commits](https://www.conventionalcommits.org/). Every commit message must start with a type prefix:

```
feat:     — new feature
fix:      — bug fix
chore:    — maintenance task
docs:     — documentation change
refactor: — code restructuring with no behavior change
test:     — adding or updating tests
```

Keep the subject line under 72 characters. Use the body for additional context when needed.

```
feat: add real-time P&L calculation to dashboard

Connects to the streaming positions API and updates
the P&L column on each tick.

Closes #42
```

## Pull Requests

1. **Write a description.** Every PR must have a summary of what changed and why.
2. **Link issues.** Reference related issues with `Closes #N` or `Relates to #N`.
3. **Request a review.** Assign at least one reviewer before marking ready.
4. **Keep PRs focused.** One logical change per PR. Split large changes into stacked PRs.
5. **Ensure CI passes.** All checks must be green before requesting review.

## Code Review

- Reviewers should **approve** or **request changes** — avoid leaving reviews in a limbo state.
- Address all review comments before merging. Resolve conversations explicitly.
- **No self-merging.** Every PR requires at least one approval from another team member.
- Prefer squash merges to keep the main branch history clean.

## Running Things Locally

```bash
bun install          # install dependencies
bun run lint         # lint
bun run typecheck    # type check
bun run test         # unit tests
bun run build        # build
```
