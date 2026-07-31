# docs.wyrdwyrks.com

Documentation site for WyrdWyrks hardware and firmware projects, including the
Celestial Wayfinder DEF CON badge.

Built with [Jekyll](https://jekyllrb.com/) and the
[Just the Docs](https://just-the-docs.com/) theme (pulled in via
`jekyll-remote-theme`), hosted on GitHub Pages at
<https://docs.wyrdwyrks.com>.

## Running the docs site locally

You'll need Ruby (3.1+) and Bundler.

Install the dependencies:

```bash
bundle install
```

Then start the local server:

```bash
bundle exec jekyll serve
```

The site is served at <http://localhost:4000> and rebuilds as you edit. Add
`--livereload` to refresh the browser automatically, or `--drafts` to include
drafts.

If you hit a `remote_theme` fetch failure or GitHub API rate limiting, export a
personal access token (no scopes needed) before serving:

```bash
export JEKYLL_GITHUB_TOKEN=your_token_here
```

## Adding a page

Create a Markdown file at the repo root with Just the Docs front matter:

```yaml
---
layout: default
title: Page Title
nav_order: 3
---
```

`nav_order` controls where the page appears in the sidebar.

## Authoring in Obsidian

Open this repo's root directory as an Obsidian vault. Required settings under
**Settings → Files and links**:

- **Use \[\[Wikilinks\]\] → off.** Jekyll can't resolve wikilinks; with this off
  Obsidian writes standard `[text](page.md)` links, which the
  `jekyll-relative-links` plugin rewrites to real URLs at build time.
- **New link format → Relative path to file.**
- **Default location for new attachments → In the folder specified below**, set
  to `assets/images`, so images land somewhere Jekyll publishes.
- **Excluded files →** add `_site` and `vendor` to keep build output out of
  search results.

Name files in kebab-case (`build-and-flash.md`) and put the display name in the
`title:` front matter — Obsidian defaults to using the note title as the
filename, which produces URLs with spaces. Every page needs the `layout`,
`title`, and `nav_order` front matter above to appear in the nav; a Templates
snippet is the easiest way to get that on every new note.
