# PNPM issue

## To reproduce

```sh
pnpm install
pnpm --filter web --prod deploy ./build
```

## Current behavior

When running pnpm deploy, a build directory is created at ./build and at ./apps/web/build. If you look at the contents of ./apps/web/build it's just the node_modules bin directory but this still shouldn't happen.

## Expected behavior

The only files written are to the <target> directory of the deploy command
