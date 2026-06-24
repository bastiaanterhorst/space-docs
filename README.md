# Sonto documentation

The help centre for the [Sonto](https://sonto.app) app for Mac and iOS, published with
[Mintlify](https://mintlify.com) from this repository. Live at
[help.sonto.app](https://help.sonto.app).

## Structure

Content is organised along the [Diátaxis](https://diataxis.fr) framework — four kinds of page, each
doing one job:

| Group | Quadrant | Purpose |
|---|---|---|
| **Start here** | — | Welcome, the Sonto Method, What's New. |
| **Concepts** | Explanation | The ideas behind the app — the *why*. |
| **Tutorials** | Tutorial | Learning-oriented, hand-held walkthroughs (the video guides + their text). |
| **How-to guides** | How-to | Goal-oriented recipes for a specific task. |
| **Reference** | Reference | Precise, scannable descriptions of every feature. |

Navigation is defined in `docs.json`. When you add a page, add it to the right group there.

## Running locally

```bash
mint dev            # preview at http://localhost:3000
mint broken-links   # check every internal link and image resolves
```

## Quality checks before publishing

- `mint broken-links` — no broken links or missing images.
- `vale .` — prose lint: UK English and on-brand vocabulary (see `.vale.ini` and `styles/Sonto/`).
- Every image has `alt` text; every reference page ends with a **Related** section.

See `CLAUDE.md` for the full authoring standards (voice, the reference template, platform-availability
convention, frontmatter).

## Writing standards in brief

- **UK English** (organise, colour, prioritise). The one exception is a US keyword that dominates
  search intent — flag it when you make that call.
- **Second person**, prerequisites up front on procedural pages.
- **Reference template:** *What it is → Where it lives (Mac/iPhone) → Fields & controls → Availability →
  Related.*
- **Be honest about platforms.** Use `<Tabs>` where Mac and iPhone differ; where iPhone genuinely lacks
  a feature (the guided planning flow, global hotkeys, the MCP server), say so with an Availability
  callout — never invent steps that don't exist.
