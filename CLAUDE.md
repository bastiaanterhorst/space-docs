# Space documentation
- This repository contains documentation for the Space app for Mac and iOS. It uses Mintlify as its documentation system.

## Working relationship
- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up information

## Project context
- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components

## Content strategy
- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability of information
- Make content evergreen when possible
- Search for existing information before adding new content. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## Frontmatter requirements for pages
- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation

## Writing standards
- Second-person voice ("you")
- **UK English** (organise, colour, prioritise, favourite, behaviour). The one exception: a US keyword
  that dominates search intent — flag the trade-off when you make that call. Note `<Badge color="...">`
  and CSS are component/code attributes, not prose — leave them as-is.
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links
- Run `vale .` and `mint broken-links` before publishing

## Structure (Diátaxis)
Pages live in one of four quadrants, wired in `docs.json`:
- **Concepts** (Explanation) — the *why*. The mental model, not steps.
- **Tutorials** — learning-oriented, hand-held walkthroughs (the video guides + their text). Keep the
  video as a supplement; the page should stand on its own in text.
- **How-to guides** — goal-oriented recipes for a specific task. Keep them lean and cross-cutting; don't
  mirror a single reference page.
- **Reference** — precise, scannable feature descriptions.

Don't outsource a page's substance to a video. Avoid duplicating content across quadrants.

## Reference page template
Every reference page follows: **What it is → Where it lives (Mac/iPhone) → Fields & controls →
Availability → Related**. Model on `reference/manage-data.mdx`, `reference/ai-with-mcp.mdx`, and
`reference/other-topics/keyboard-shortcuts.mdx`.

## Platform honesty
Use `<Tabs>` ("Mac" / "iPhone & iPad") where steps diverge. Where iPhone genuinely lacks a feature —
the guided planning flow, global hotkeys, the MCP server — state it with an Availability `<Warning>`.
Never write steps for a flow a platform doesn't have. Source of truth for capabilities:
`../space-content/docs/space-capabilities.md`.

## Git workflow
- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Do not
- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification