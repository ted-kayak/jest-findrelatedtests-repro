# --findRelatedTests exit 0
This is a minimal reproduction for a bug where using the `--findRelatedTests` flag will cause Jest to exit with code 0 even though the console output is saying the script will exit with code 1.

Reproduction:
```sh
npm install
npm test             # exits 1 (expected)
npm run test:related # exits 0 (bug)
```

