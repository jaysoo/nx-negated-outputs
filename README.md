# Nx Next.js starter

Adapted from https://vercel.com/templates/next.js/turborepo-next-basic

I'm trying to set the outputs to just `.next` without `.next/cache`. However, when running the build, it just hangs forever.

```
npx nx build web
```

See the `project.json` with the outputs configured as:

```
"outputs": [
  "{projectRoot}/.next",
  "!{projectRoot}/.next/cache"
]
```

If you remove the second `!` negated output, then the build succeeds.
