# scottpuppylu.github.io — Diff Check / 哥布林大調查 root site

This repository is the **free root landing page and site-verification host** for Diff Check / 哥布林大調查. It is served
at https://scottpuppylu.github.io/.

| What | Where |
|---|---|
| Canonical application source | [scottpuppylu/valorant-squad-analytics-v2](https://github.com/scottpuppylu/valorant-squad-analytics-v2) |
| Full public demo (synthetic) | https://scottpuppylu.github.io/valorant-squad-analytics-v2/ |
| This repository | `site/` only: a static landing page, `.nojekyll` and `site-control.txt` |

## What this repository does NOT contain

- No application code, analytics, collector or data snapshots: it is not a copy of the V2 app.
- No canonical match database, and no real player data, Riot IDs, account ids or match ids.
- No provider credentials, API keys, tokens or secrets. The Pages workflow uses zero secrets.
- No trackers, cookies, external fonts or external scripts.

## Root control proof

`site/site-control.txt` is served at https://scottpuppylu.github.io/site-control.txt. It only proves that this repository
can serve a plain text file at the domain root. It is **not** a Riot verification token.

## riot.txt (intentionally absent)

`riot.txt` is **not** present until Riot supplies its exact verification content. The workflow fails if it appears early.
Never invent or guess the token.

When Riot provides the exact contents:
1. Put the exact text, with nothing before or after it, in `site/riot.txt`, and remove the guard step in
   `.github/workflows/pages.yml` in the same commit.
2. Push to `main` so the site deploys.
3. Verify https://scottpuppylu.github.io/riot.txt.
4. Confirm an exact byte/text match with Riot's string.
5. Run Riot's site verification.
6. Remove the file afterwards if Riot's instructions require it.

## Domain strategy

- `ROOT_SITE_STRATEGY = GITHUB_USER_SITE_FREE`
- `OWNED_CUSTOM_DOMAIN = DEFERRED_FALLBACK`, used only if Riot rejects the github.io root site.
- No custom domain, DNS records, Cloudflare or Vercel.

## Contact

Privacy / data requests: [casper880115@gmail.com](mailto:casper880115@gmail.com)

哥布林大調查 isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially
involved in producing or managing Riot Games properties. Riot Games, and all associated properties are trademarks or
registered trademarks of Riot Games, Inc.
