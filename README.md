# Do not delete this repo

It contains no project code. Its only job is to keep the **old** portfolio URL working:

```
https://josephnguyen010-prog.github.io/Joseph-Nguyen-Portfolio-/   (old, this repo)
        -> https://josephnguyen010-prog.github.io/Joseph-Nguyen-Portfolio/   (live site)
```

## Why it exists

The portfolio repo was renamed to drop a trailing hyphen. GitHub permanently
redirects renamed *repo* URLs, but it does **not** redirect GitHub *Pages*
URLs — so the old site address started returning a hard 404.

That old address had already gone out on job applications, where it cannot be
corrected after the fact. This repo makes those links resolve instead of dying.

## How it works

- `index.html` redirects the root, preserving the `#hash` anchor.
- `404.html` catches deep links (`/arrivals/`, the resume PDF, ...) and rewrites
  only the repo segment, so the rest of the path survives. GitHub Pages serves
  this file for any path it cannot resolve.

Both use a JS redirect with a `<meta http-equiv="refresh">` fallback, plus a
visible link if neither fires.

## Retiring it

Safe to delete once the old link is no longer in circulation anywhere —
applications, resumes, LinkedIn, email signatures. There is no rush; it costs
nothing to leave up.
