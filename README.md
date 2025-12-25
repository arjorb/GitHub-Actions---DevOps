# GitHub Actions

This repository contains concise DevOps automation and CI/CD pipeline examples using GitHub Actions.

## Minimal Node.js Example

A minimal Node.js project is included to ensure the workflows run successfully:
- [`index.js`](index.js:1): Minimal executable script
- [`package.json`](package.json): Project manifest with `start`, `test`, and `build` scripts

### Usage

```bash
npm start   # Runs index.js
npm test    # Always succeeds (no tests specified)
npm build   # Always succeeds (no build step required)
```

## Workflows

### Node.js CI ([`.github/workflows/node-ci.yml`](.github/workflows/node-ci.yml:1))
Runs on every push and pull request. Installs dependencies, runs tests, and executes a build step for the minimal Node.js project. Ensures the pipeline passes even with minimal code.

### Environment-Specific Deployments ([`.github/workflows/env-specific-deployments.yml`](.github/workflows/env-specific-deployments.yml:1))
Triggers on pushes to `main` and `develop` branches. Sets deployment environment variables based on branch, then simulates a deployment step with environment-specific output. Uses a secret token for deployment.

## License
MIT License.
