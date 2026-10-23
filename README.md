# ci-cd-lab

Small Express 5 app with a GitHub Actions CI pipeline (ESLint, Mocha/Chai/Supertest, c8 coverage).

## Requirements

- Node.js 24+
- Yarn 4 (`corepack enable`)

## Commands

| Command          | Purpose                                   |
| ---------------- | ----------------------------------------- |
| `yarn install`   | Install dependencies                      |
| `yarn start`     | Run the server on port 3000 (or `$PORT`)  |
| `yarn lint`      | Run ESLint                                |
| `yarn test`      | Run the Mocha test suite                  |
| `yarn coverage`  | Run tests with c8, HTML report in `coverage/` |

`GET /` returns `Hello, GitHub Actions!`.

## CI

`.github/workflows/ci.yml` runs on pushes and pull requests to `main`: install (`--immutable`), lint, test, coverage, then uploads the `code-coverage-report` artifact.
