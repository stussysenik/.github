# .github

Organization-wide GitHub configuration for stussysenik.

## What this does

- **CodeQL** — semantic code analysis for JavaScript/TypeScript, Python, Ruby on every push. Catches SQL injection, XSS, path traversal, auth bypasses (the Carlini-class vulnerabilities).
- **Gitleaks** — secret scanning on every push to prevent credential leaks.
- **Dependabot** — automated dependency security updates for npm, pip, bundler, and GitHub Actions.

These workflows automatically apply to all public repositories that don't have their own workflow files.
