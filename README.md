# Utakata

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](LICENSE)
[![Vibe Coded](https://img.shields.io/badge/✨-vibe_coded-blueviolet)]()

A dark, minimal Ghost theme built around a timeline layout. No external dependencies, no tracking. 

> [!CAUTION]
> **Vibe Disclaimer**: The original Tidslinje was 100% vibe-coded in collaboration between a human architect and an agentic AI.
> This fork, Utakata, takes it one step further — maintained by someone who is technically literate enough to be dangerous but has absolutely no idea what they're doing, and just wanted a nice theme for their personal blog. Code quality is best described as "enthusiastic". By using this, you accept that reality is subjective, that "it works on my machine" is a valid deployment strategy, and that aesthetic intent outweighs structural integrity.

## Features

- Timeline-based post listing with configurable density and icon positions
- Multiple color palettes (Default, Dracula, Catppuccin, Nordic Forest, Warm Earth, Cyberpunk)
- Six navigation styles (Pill, Underline, Minimal, Brackets, Block, Cursor)
- Three font families (Serif, Sans-serif, Monospaced) with adjustable size
- Micro posts for short-form content
- Previous/next post navigation at the bottom of each post
- Reading progress bar on post pages
- Minimal JS (related posts, scroll animations), no third-party requests
- Swedish and German localization

## Setup

### Installation

Package and upload:

```bash
npm run zip
```

Upload `utakata.zip` via **Ghost Admin > Settings > Design > Change theme**.

### Configuration

- **Featured posts**: Upload the included `routes.yaml` in **Settings > Labs** to pin featured posts.
- **Search**: Add a nav item with label `Search` and URL `#/search`.
- **Comments**: Enable via **Settings > Membership > Commenting**.

### Theme Settings

All of these are in **Ghost Admin > Design**:

| Setting | Options |
|---|---|
| Color palette | Default, Dracula, Catppuccin, Nordic Forest, Warm Earth, Cyberpunk |
| Font | Serif, Sans-serif, Monospaced |
| Body font size | Small, Default, Large |
| Container width | Narrow, Normal, Wide |
| Show site icon | On / Off |
| Icon framing | Round, Squircle, Rounded, Sharp |
| Navigation style | Pill, Underline, Minimal, Brackets, Block, Cursor |
| Navigation size | Extra Small – 2X Large |
| Timeline density | Compact, Comfortable, Spacious |
| Timeline icon position | Standard, Left, Right, None |
| Show reading time | On / Off |
| Show reading progress bar | On / Off |

Post display toggles (author, date, tags, related posts, excerpts) and a Welcome Mat opt-in CTA are also available.

For a complete guide to all settings, custom page templates, and features, see **[docs.md](docs.md)**.

### Timeline Icons

Put an emoji in the **Description** field of an **Internal Tag** (the ones starting with `#`). The first internal tag with a description is used as that post's timeline icon. Falls back to `✍️`.

### Micro Posts

Tag a post with `#micro` to turn it into a short-form entry — no title, no "Read more" link, just the content inline on the timeline with a small `#` permalink.

### Localization

Set your Ghost publication language (`Settings > General > Publication Language`). Swedish translations are in `locales/sv.json`, German translations are in `locales/de.json`.

## CSS Overrides

Override any theme variable via **Code Injection**:

```html
<style>
  :root {
    --bg-color: #1e1e1e;
    --card-bg: #252525;
    --text-color: #e0e0e0;
    --text-muted: #a0a0a0;
    --accent-color: #6cb6ff;
    --heading-color: #fff;
    --border-color: #333;
    --timeline-line-color: #444;
    --code-bg: #111;
  }
</style>
```
## Credits

Based on [Tidslinje](https://github.com/klppl/tidslinje) by [klppl](https://github.com/klppl).

## License

[GPL-3.0](LICENSE)
