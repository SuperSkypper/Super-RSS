# 📡 Super RSS

[![Release](https://img.shields.io/github/v/release/SuperSkypper/super-rss)](https://github.com/SuperSkypper/super-rss/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Min App Version](https://img.shields.io/badge/obsidian-1.6.6%2B-7c3aed)](https://obsidian.md)

An Obsidian plugin that fetches RSS feeds and saves articles as notes in your vault.

Available in the Obsidian Community Plugins directory.

## ✨ Features

**🗒️ Note templates**
- Control filename, frontmatter, and content using template variables.
- Override global settings per feed (fetch interval, template, cleanup rules).

**📁 Feed organization**
- Batch edit feeds.
- Group feeds into collapsible folders.
- Folders rename automatically when feeds are moved or edited.

**🔍 Deduplication**
- Scans your RSS folder before importing to avoid duplicate notes.
- Tracks imported entries in a local database.

**🧹 Auto-cleanup**
- Delete old notes automatically after a configurable period.
- Choose whether to measure age by publication date or saved date.
- Skip cleanup for notes that have a specific property checked.

**✅ Mark as read**
- URI handler lets you mark items as read from within a note.
- Optional: delete the note automatically when marked as read.
- Mark as read in Obsidian Bases.

**🖼️ Images**
- Link images from articles to your notes.
- Optional: download images locally to your vault.

**▶️ YouTube**
- Automatically detects YouTube RSS feeds from a channel link.
- Picks the highest available thumbnail resolution.
- Fetches video duration for YouTube links.
- Optional: toggle to skip Shorts or live streams.

## 📦 Installation

### Community plugins

Install **Super RSS** from **Settings → Community plugins** inside Obsidian.

### Manual

1. Download `manifest.json`, `main.js`, and `styles.css` from the [latest release](https://github.com/SuperSkypper/super-rss/releases/latest).
2. Create the folder `<Vault>/.obsidian/plugins/super-rss/`.
3. Copy the three files into that folder.
4. Reload Obsidian and enable **Super RSS** under **Settings → Community plugins**.

Requires Obsidian **1.6.6** or later. Works on desktop and mobile.

## 📖 Template variables

| Variable | Value |
| --- | --- |
| `{{title}}` | Article title |
| `{{author}}` | Author name |
| `{{datepub}}` | Publication date from the feed |
| `{{datesaved}}` | Date the note was created |
| `{{snippet}}` | Short description or summary |
| `{{feedname}}` | Name of the source feed |
| `{{link}}` | Original article URL |
| `{{image}}` | Local or remote image path |
| `{{duration}}` | Video duration (YouTube only) |
| `{{#tags}}` | Tags derived from feed categories |
| `{{content}}` | Full article content |

## 🛠️ Development

```bash
npm install
npm run dev       # watch build
npm run build     # type-check and bundle to main.js
npm run lint
```

Copy `manifest.json`, `main.js`, and `styles.css` to `<Vault>/.obsidian/plugins/super-rss/`, then reload Obsidian and enable **Super RSS**.

## 💬 Support

- [GitHub Issues](https://github.com/SuperSkypper/super-rss/issues) — bug reports and feature requests
- [Ko-fi](https://ko-fi.com/superskypper)
- [X / Twitter](https://x.com/SuperSkypper)

## 📄 License

MIT — see [LICENSE](LICENSE).

## ✍️ Note from the author

I am not a programmer. I built Super RSS because it was a tool I needed for my own workflow, and I decided to share it in case it helps other people too.

This plugin was created over roughly four months using the tools Claude and Codex.
