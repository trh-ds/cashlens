# Contributing to CashLens

Thanks for helping. CashLens is **pre-alpha**: most of the codebase does not exist yet, so the
[roadmap](README.md#roadmap) is the best place to find work. Issues labelled
[`good first issue`](https://github.com/trh-ds/cashlens/labels/good%20first%20issue) are scoped for newcomers.

By participating you agree to the [Code of Conduct](CODE_OF_CONDUCT.md).

## Golden rule: no real financial data

**Never commit real bank statements, account numbers, IFSC + account pairs, GSTINs, PANs, Aadhaar
numbers or any personal data** — not in code, fixtures, notebooks, screenshots, issues or PRs.
Use the synthetic Hugging Face dataset, AA sandbox data, or generated fixtures. `data/raw/` and `*.pdf`
are git-ignored for this reason.

## Setup

```bash
git clone https://github.com/trh-ds/cashlens.git
cd cashlens
cp .env.example .env
pip install pre-commit && pre-commit install
```

Per-service setup will be documented in the [README](README.md#getting-started) as each service lands.

## Branch naming

`<type>/<short-description>`, e.g. `feat/forecast-baseline`, `fix/balance-recompute`, `docs/readme-data`.

## Commit messages

Follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```text
feat(ml): add Prophet baseline for 90-day net inflow
fix(data): recompute running balance from opening_balance
docs: document dataset quirks
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`, `ci`, `perf`.

## Pull request checklist

- [ ] One logical change per PR; link the issue (`Closes #123`)
- [ ] `pre-commit run --all-files` passes (ruff, ruff-format, whitespace, private-key check)
- [ ] Tests added or updated for code changes
- [ ] CI is green
- [ ] Docs updated if behaviour changed
- [ ] No real financial or personal data anywhere in the diff

## Reporting security issues

See [SECURITY.md](SECURITY.md). Do not open public issues for vulnerabilities.
