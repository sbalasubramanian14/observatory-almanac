# observatory-almanac

Published data bundle for [observatory](https://github.com/sbalasubramanian14/observatory).

**This repository is written by a machine.** Commits here are produced by the
observatory pipeline's publish stage. Nothing in it is hand-edited, and pull
requests against it will not be reviewed.

## What is here

Pre-ranked, deduplicated AI news stories as static JSON, read directly by the
web and mobile clients over a CDN. Files are content-addressed, so every data
file is immutable and cacheable forever; only `manifest.json` is refetched.

## What is deliberately not here

- **Full article text.** Republishing publishers' article bodies would be
  redistribution of copyrighted work. Only titles, canonical links, metadata,
  and observatory's own generated summaries and analysis are published. Full
  text stays in the local store.
- **Reader behaviour.** Opens, dwell times, dismissals and the interest
  profile never leave the reader's own devices. Personalization runs entirely
  client-side, which is why the published feed is ranked by reader-independent
  importance only.

## Retention

Files outside a rolling window are pruned by the publish stage and the history
is periodically squashed. This repository is a distribution channel, not an
archive; the local store is the system of record.
