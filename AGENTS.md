# kennan-grant.github.io - agent instructions

This is Kennan's public GitHub Pages site.

## Ground Rules

- Keep the site simple, static, and easy to reason about.
- Do not introduce build tooling, package managers, frameworks, analytics, external scripts, external fonts, or network dependencies unless explicitly requested.
- Preserve public URLs whenever possible. Paths here may be shared externally.
- Do not publish private drafts, source repos, local notes, or generated source/build files unless the user explicitly asks for that specific content to be public.
- When adding generated artifacts from another repo, copy only the deployable output into this repo.

## Resume

Resume pages live under:

`/resume/`

The main resume page is:

`/resume/index.md`

This is a public-facing Markdown/Jekyll page using the default layout. Edit it directly only when the user asks to update resume content or presentation. Preserve front matter unless intentionally changing the page layout/title.

## Study Artifacts

Study pages live under:

`/study/<topic>/`

The performance course should live at:

`/study/performance-fundamentals/index.html`

That file is generated from the private `cs-study` repo. Do not edit it directly here; regenerate it from the source repo and copy the built HTML into place.
