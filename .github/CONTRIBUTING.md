# Contributing to Integral-Productivity Repos

## Commit message conventions

All commits use [Conventional Commits](https://www.conventionalcommits.org/):

| Prefix | When to use |
|---|---|
| `feat:` | Adds a new capability |
| `fix:` | Corrects a bug |
| `chore(scope):` | Maintenance — dependency bumps, config changes, housekeeping |
| `docs:` | Documentation only |
| `ci:` | CI/CD workflow changes |

The PR title becomes the squash-commit subject — write it as a Conventional Commit.

## Branch naming

| Branch prefix | Meaning |
|---|---|
| `claude/<slug>` | Authored by a Claude Code agent. Auto-merges on green CI. |
| `<your-name>/<slug>` | Human-authored feature or fix branch. Requires manual merge. |

`claude/*` branches are created automatically when you invoke the Claude agent via an
`@claude` mention in an issue or PR comment. Do not create them by hand.

## Pull request rules

- **Do not open draft PRs.** Auto-merge only fires on ready-for-review PRs. If your work
  is incomplete, keep it local until it's ready.
- **Squash merge only.** Rebase and merge-commit are disabled. The PR title + description
  become the single squash commit.
- **Closing keywords must appear in the PR description or a commit message** — not in a
  PR review comment. GitHub only parses closing keywords from those locations.
  Use: `Closes #123`, `Fixes #456`, `Resolves #789`.

## CI requirements

All Tier 1 and Tier 2 PRs must pass:

- **Typecheck** — `pnpm typecheck`
- **Build** — `pnpm build`
- **Test** — `pnpm test`
- **Dependency Review** — no new dependencies with known moderate+ vulnerabilities

The branch must be up to date with `main` before merging (enforced by the Tier 1 org
ruleset).

## Auto-merge

Dependabot PRs (patch/minor updates) and `claude/*` branches merge automatically when CI
is green. Major-version Dependabot updates and human-authored branches require manual merge.
