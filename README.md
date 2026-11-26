# sandbox-python-static

Made from [Jomaries777/template-repo-ci](https://github.com/Jomaries777/template-repo-ci).
Stack: `python` (`stacks/python/`). Deploy target: `github-pages` (`deploy.yml`).

## Work

Every change starts as `intent/<id>-<slug>/intent.md` (run `/intent` in Claude
Code), then `spec.md` and `plan.md`, then a PR. Only `ci-ok` is required to
merge; the owner approves.

## Commands

| Command | What it does |
|---|---|
| `make lint` / `make fmt` | Repo and stack linters / formatters |
| `make test` | Script tests and the stack's unit tests |
| `make typecheck` / `make build` | Type-check / build the deploy artifact |
| `make acceptance` | Acceptance suite against a local container |
| `make smoke URL=<url>` | `prod-safe` smoke tests against a URL |
| `make doctor` | Check repo settings, secrets and the deploy target |
