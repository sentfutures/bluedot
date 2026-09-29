# Sentient Futures fork

This is Sentient Futures' fork of [bluedotimpact/bluedot](https://github.com/bluedotimpact/bluedot),
which BlueDot Impact licenses under the [GNU AGPL v3](./LICENSE). So this fork is **public**, and
everything in it, including code we write, is AGPL and public too.

## Rules

- **No Kairos code here, ever.** That means anything from `sentfutures/kairos-shared`,
  `sentfutures/sf-dashboard` or Kairos's own repo. We have it under a confidential code sharing
  agreement that forbids publishing it. Ideas and patterns are fine; code isn't.
- **No code from here in our private repos either.** AGPL code copied into a private app we serve
  over the web would oblige us to publish that app's source. Our private systems talk to what we
  build here over HTTP or through Airtable, never by importing it.
- **No secrets or personal data.** API keys, Airtable base and table IDs, and participant names
  or emails go in environment variables (`.env.local`, which is gitignored), never in commits.
  Secret scanning and push protection are on, but they only catch known key formats.
- **Deploy what we build here as its own service, with a visible "Source code" link** to this
  repo. AGPL section 13 entitles anyone using a modified version over a network to its source.
- **Keep BlueDot's licence and copyright notices**, and log our changes, with dates, under
  "Our changes" below (AGPL section 5a).

## Working here

- Our work goes on `master` alongside BlueDot's. To pull in BlueDot's updates, press **Sync fork**
  on GitHub, or:
  ```bash
  git remote add upstream https://github.com/bluedotimpact/bluedot.git   # once
  git fetch upstream && git merge upstream/master
  ```
- **GitHub Actions is off.** BlueDot's workflows deploy BlueDot's own website. Turn Actions back
  on only after replacing `.github/workflows/` with ours.
- Start with BlueDot's [`CLAUDE.md`](./CLAUDE.md) and
  [`DEVELOPMENT_HANDBOOK.md`](./DEVELOPMENT_HANDBOOK.md), then
  [`apps/meet`](./apps/meet): the attendance join page, the first thing we're adapting.

## Our changes

| Date       | Change                                              |
| ---------- | --------------------------------------------------- |
| 2026-09-28 | Added this file and `.claude/CLAUDE.md`. No code changes yet. |
