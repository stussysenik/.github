<div align="center">

# .Github

Community health files, reusable CI/CD workflows, and project standards

[![Language](https://img.shields.io/github/languages/top/stussysenik/.github?style=flat-square)]()
[![Last Commit](https://img.shields.io/github/last-commit/stussysenik/.github?style=flat-square)]()
[![Repo Size](https://img.shields.io/github/repo-size/stussysenik/.github?style=flat-square)]()

</div>

---

## Quick Start

```bash
git clone https://github.com/stussysenik/.github.git
cd .github
```

## What's Here

### Community Health Files

| File | Purpose |
|------|---------|
| `CODE_OF_CONDUCT.md` | Contributor Covenant |
| `CONTRIBUTING.md` | How to contribute |
| `SECURITY.md` | Security vulnerability reporting |
| `SUPPORT.md` | Where to get help |
| `FUNDING.yml` | Sponsorship links |

### Issue & PR Templates

| File | Purpose |
|------|---------|
| `.github/ISSUE_TEMPLATE/bug_report.yml` | Structured bug reports |
| `.github/ISSUE_TEMPLATE/feature_request.yml` | Feature request form |
| `.github/ISSUE_TEMPLATE/config.yml` | Issue template chooser config |
| `.github/PULL_REQUEST_TEMPLATE.md` | PR template (what/why/how) |

### Reusable Workflows

Call these from any repo with `uses: stussysenik/.github/.github/workflows/<name>@main`.

| Workflow | Purpose |
|----------|---------|
| `ci-node.yml` | Node.js CI (npm/pnpm/bun, lint, typecheck, test, build) |
| `ci-python.yml` | Python CI (ruff, mypy, pytest) |
| `ci-swift.yml` | Swift CI (SPM or Xcode, iOS/macOS) |
| `label-sync.yml` | Sync repo labels from config |
| `release-please.yml` | Automated releases |
| `stale.yml` | Close inactive issues/PRs |

### Config

| File | Purpose |
|------|---------|
| `.github/dependabot.yml` | Dependabot for GitHub Actions |
| `.github/labels.yml` | Default label definitions |

## Usage

### Calling a reusable workflow

```yaml
# .github/workflows/ci.yml in your repo
name: CI
on: [push, pull_request]
jobs:
  ci:
    uses: stussysenik/.github/.github/workflows/ci-node.yml@main
    with:
      package-manager: bun
      node-version: "22"
```

### How defaults work

GitHub automatically uses files from this repo as defaults for any repository that doesn't define its own. This includes the code of conduct, contributing guide, security policy, support docs, issue templates, and PR template.
