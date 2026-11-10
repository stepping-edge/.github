# Contributing

These rules apply to every repo in the Stepping Edge org unless the repo's own CONTRIBUTING.md says otherwise.

## Branches

`main` is always deployable. Never push to it directly. Work on a short-lived branch:

| Branch | Use for | Example |
| --- | --- | --- |
| `feature/<ticket>-<short-name>` | New work | `feature/SE-142-checkout-page` |
| `fix/<ticket>-<short-name>` | Bug fixes | `fix/SE-151-login-timeout` |
| `hotfix/<short-name>` | Urgent production fixes | `hotfix/payment-null-check` |
| `release/<version>` | Optional release stabilisation | `release/1.4.0` |

## Pull requests

1. Open a pull request into `main` and fill in the template.
2. Get one approval from someone other than you. Changes to payments or personal data need two.
3. Wait for CI to pass.
4. Merge with **Squash and merge**. The PR title becomes the commit message, so write it as a [Conventional Commit](https://www.conventionalcommits.org/): `feat: add checkout page`, `fix: handle login timeout`.

## Releases

Tag releases `v<major>.<minor>.<patch>` and publish GitHub Release notes.

## Secrets

Never commit passwords, API keys, tokens or `.env` files. Store them as repo Actions secrets named by environment, e.g. `PROD_DB_URL`, `STAGING_DB_URL`.

## Freelancers

If you have Read access, fork the repo, push to your fork, and open a pull request from it. A project lead reviews and merges.
