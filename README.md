# Open Eppic — The Atom Demo

**This is a prototype, not a product.** It exists to make one idea legible
in one sitting:

> create original → activate → derive → render the unbreakable lineage line.

Built and maintained from the main Open Eppic project. This repo exists only
to host the standalone demo via GitHub Pages — it is not the platform, not a
launch, and not where real design or engineering decisions live. Those live
in the main `Open-Eppic` project.

## What this is not

- **Not a member-facing instance.** There is no real license, no export, no
  moderation, and nothing here has been legally reviewed. Real creator
  originals do not belong in this instance, ever — the whole point of the
  boundary is that nothing here is a promise to anyone.
- **Not a finished editor experience.** Content is a plain title/summary/
  notes form. The typing-lag and editor-feel questions this build cares
  about are untested here.
- **Not evidence that anything is "solved."** A good reaction to this demo
  is not evidence that the underlying design or demand questions are
  settled — see the main project's `docs/atom-prototype.md` for what this
  prototype does and does not prove.

## Try it

Open the [live demo](https://YOUR-GITHUB-USERNAME.github.io/REPO-NAME/) and
sign in as either seed account:

| Account | Role |
|---|---|
| `maren@demo.openeppic.test` | World owner — has activated originals |
| `theo@demo.openeppic.test` | Sub-creator — has derived from Maren's work |

Password for both: `demo-atom-2026`

**This password is intentionally public.** Everything in this instance is
disposable, founder-authored seed content — there is nothing here worth
protecting with a real credential. What that does mean: **this is a shared,
public instance.** Anyone with the link can sign in as either account and
create, activate, derive, remove, or publish things. If you find it in a
confusing or broken state, that's likely another visitor mid-exploration,
not a bug — the underlying database can be reseeded from the main project's
migrations if it needs a clean reset.

## How it's built

A single static HTML file, no build step, no framework — `index.html` talks
directly to a live Supabase project via `supabase-js` over the public
publishable key. Row-Level Security in Postgres is the actual security
boundary, not anything in this file; every rule about who can see, edit,
activate, derive, or remove what is enforced server-side and is testable
independent of this UI. See the main project's
`supabase/migrations/` for the schema and `docs/atom-prototype.md` for the
full design writeup, invariants, and open questions.

## License

Part of the Open Eppic project, licensed AGPL-3.0-or-later, matching the
main repository. Fork it, run it yourself, point it at your own Supabase
project — that's the point.
