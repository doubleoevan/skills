---
name: git-discipline
description: >
  Git workflow rules. Use whenever changes have been made to files and a
  commit is being considered, suggested, or written: every commit message,
  every commit, every push decision. Covers commit approval, the never-push
  rule, diff review, and Conventional Commits message format.
---

# Git Discipline

### Commits require approval

Ask before running `git commit`. "Go ahead" at session start pre-approves
commits for that session. NEVER push; pushing is always manual and human.
Before suggesting a commit, review the full diff: the message must describe
what actually changed, not what was intended.

### Commit message format: Conventional Commits

`type: subject` with a lowercase imperative subject, no trailing period,
under 72 characters.

Types: feat, fix, chore, docs, refactor, test, build, ci.

- feat means user-facing product capability only. Tooling, scaffolding,
  hooks, and developer experience are chore.
- Scope is optional and lowercase: `feat(db): add topic schema`.
- Breaking changes: append `!` after the type and explain in the body.

### Commit message body

Plain English, readable with zero project context. Never reference internal
planning artifacts: no "Day N", phase numbers, sprint names, or task labels.
Bullets over prose for multi-part changes. Wrap at 72 characters.

    chore: add agent tooling, enforcement hooks, and local model proxy

    - LiteLLM proxy via docker compose with three model aliases
    - blocking hooks for comment discipline and single-package structure