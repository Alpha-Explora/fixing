# fixing

Created by ALPHACI as a Node.js service standalone repository.

This starter already includes source files, package scripts, TypeScript, ESLint, Jest coverage, SonarQube metadata, branch protections, and ALPHACI workflow files that match the selected stack. Use it as the first working baseline, then replace the starter code with your application code.

## Project structure

- `src/index.ts` is the starter Node.js entrypoint.
- `tests/unit/index.spec.ts` verifies the exported service name.
- Docker scaffolding starts `dist/index.js`, matching the TypeScript build output.

## Branch strategy

| Branch  | Purpose |
|---------|---------|
| main    | Production - protected |
| uat     | Integration and test - protected |
| develop | Development integration - unprotected, no CI pipeline |

## CI/CD

Workflow files live in `.github/workflows/`. The CI pipeline runs on `uat` and `main` only. `develop` and user-created branches do not trigger workflows. Push to `uat` to trigger your first run.

## Getting started

```bash
npm install
npm run lint
npm test
npm run build
```

Create a feature branch, open a pull request into `uat`, and let ALPHACI promote green changes to `main`.