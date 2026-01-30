# slidev-theme-tokyo-python

A [Slidev](https://sli.dev/) theme designed for the Tokyo Python Meetup.

## Features

- **Title Slide**: Automatically includes Tokyo Python branding with a custom layout.
- **Tokyo Branding**: Uses the official Tokyo Python red (`#f12e24`) for headings.
- **Typography**: Optimized with Calibri for body text and JetBrains Mono for code blocks.
- **Slick Code Blocks**: Light gray backgrounds with rounded corners and consistent padding.
- **Optimized Spacing**: Tightened layouts to ensure content fits beautifully on every slide.

## Installation

Add this theme to your Slidev project:

```bash
npm install slidev-theme-tokyo-python
```

## Usage

In your `slides.md` file, set the theme:

```yaml
---
theme: tokyo-python
---
```

### Title Slide

To use the branded title slide, use the `title` layout:

```markdown
---
layout: title
---

# Your Talk Title
## Your Subtitle or Name
```

The background and Python logo are automatically included by default.

### Customizing Images

If you want to override the default images on the title slide:

```yaml
---
layout: title
topImage: /path-to-your-logo.png
bottomImage: /path-to-your-footer.png
---
```

## Development

- `npm run dev`: Start the development server.
- `npm run build`: Build the presentation for production.
- `npm run export`: Export the presentation as a PDF.
