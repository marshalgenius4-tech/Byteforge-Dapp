# Byteforge-Dapp Frontend & Action Toolkit

The frontend and GitHub Action runner toolkit for Byteforge-Dapp — measuring, comparing, and guarding Soroban smart contract resource costs in CI pull requests.

## Architecture

```text
frontend/
├── src/                # TypeScript source code
│   ├── action.ts       # GitHub Action entrypoint
│   ├── cli.ts          # Byteforge-Dapp CLI runner
│   ├── measurement.ts  # Contract execution and simulation runner
│   ├── diff.ts         # Resource delta calculation & comparison
│   ├── threshold.ts    # Policy rules & threshold evaluation
│   ├── comment.ts      # Markdown report & GitHub PR comment generator
│   └── config.ts       # Zod schema validation for configs & fixtures
├── bundled/            # Compiled standalone Node.js action bundles
├── comment/            # Dedicated PR comment action definition
├── scripts/            # Build, verification, and provenance utilities
├── test/               # Vitest unit test suite
├── tests/              # End-to-end and integration test suites
├── package.json        # Dependencies and build scripts
└── tsconfig.json       # TypeScript compiler configuration
```

## Building the Frontend

Build the TypeScript sources:
```bash
npm run build
```

Bundle the self-contained GitHub Action entrypoints:
```bash
npm run bundle
```

Typecheck the codebase:
```bash
npm run typecheck
```

## Testing

Run unit tests with Vitest:
```bash
npm run test:vitest
```

Run complete test suite:
```bash
npm test
```
