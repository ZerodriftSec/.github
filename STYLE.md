# Zerodrift Code Style

Formatting is automated. Style disputes should be resolved by tooling and documented repository conventions.

## General

- Use lowercase kebab-case for repository names.
- Prefer precise names over generic names like `audit`, `tools`, or `app`.
- Keep READMEs current with install, run, test, and security instructions.
- Keep generated files out of diffs unless they are part of the release artifact.
- Treat public repositories as portfolio surfaces: descriptions, topics, and READMEs matter.

## Markdown

- Use sentence-case prose and concise headings.
- Include a status section in every README.
- Use tables for report indexes and command summaries.
- Run Prettier where available.

## Python

- Format with `ruff format`.
- Lint with `ruff check`.
- Use type hints for public functions and shared modules.
- Prefer `pytest` for tests.

## TypeScript and JavaScript

- Use TypeScript for new application or library code.
- Format with Prettier.
- Lint with ESLint.
- Prefer strict TypeScript settings for maintained packages.

## Solidity

- Format with `forge fmt`.
- Pin compiler versions for production code.
- Avoid floating pragmas in audited or production contracts.
- Add tests for security-critical behavior.

## Move

- Use package-level documentation.
- Keep modules small and named by protocol role.
- Add tests for capability, signer, object ownership, and abort-path behavior.

## Shell

- Format with `shfmt`.
- Lint with `shellcheck`.
- Use `set -euo pipefail` for scripts unless there is a documented reason not to.

## EditorConfig

Recommended baseline:

```ini
root = true

[*]
charset = utf-8
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
indent_style = space
indent_size = 2

[*.py]
indent_size = 4

[*.{sol,move,rs,go}]
indent_size = 4

[Makefile]
indent_style = tab
```
