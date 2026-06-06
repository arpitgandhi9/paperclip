# RTK Token-Saving Mode

RTK is a token-optimized CLI proxy for agent shell work:
https://github.com/rtk-ai/rtk

## Rule

When `rtk` is installed, prefer RTK wrappers for exploratory commands and
validation output so agent runs spend fewer tokens on shell noise.

Examples:

```sh
rtk git status
rtk git diff
rtk find "*.ts" .
rtk grep "pattern" .
rtk read server/src/index.ts -l aggressive
rtk test pnpm test
rtk err pnpm -r typecheck
```

Use raw shell commands when RTK does not support the command, when exact full
output is required, or when a command is already intentionally small.

## Checks

```sh
rtk --version
rtk gain
```
