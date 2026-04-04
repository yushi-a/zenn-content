# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Start local preview server (http://localhost:8000)
npx zenn preview

# Create a new article
npx zenn new:article --slug 記事のスラッグ

# Create a new book
npx zenn new:book
```

## Repository Structure

This is a [Zenn](https://zenn.dev) content repository managed with `zenn-cli`.

- `articles/` — Tech articles as Markdown files. Filenames are either auto-generated UUIDs or custom slugs (12+ alphanumeric chars).
- `images/<article-slug>/` — Images for each article, referenced in Markdown as `/images/<slug>/<filename>`.
- `books/` — Book content (currently unused).

## Article Frontmatter

Every article requires this frontmatter:

```yaml
---
title: "記事タイトル"
emoji: "emoji"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["topic1", "topic2"]  # up to 5 topics
published: true  # false = draft
---
```

## Publishing

Articles are published to Zenn by pushing to the `main` branch on GitHub. Setting `published: true` in frontmatter makes the article public; `false` keeps it as a draft.
