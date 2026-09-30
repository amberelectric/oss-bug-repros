# knip: Serverless `${file()}` in `plugins` throws

```sh
npm install
npx knip
```

Actual: `ERROR: Error loading serverless.yml (config.plugins?.filter is not a function)`, exit code 2, `src/hello.js` reported as unused and `serverless-offline` reported as an unused devDependency.

Expected: `${file(./shared.yml):plugins}` is resolved, so there are no findings.
