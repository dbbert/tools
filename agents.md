# Agents

Instructions for AI agents working on this repository.

## Project overview

A collection of self-contained, browser-based utility tools. Each tool is a single HTML file with embedded CSS and JavaScript — no build step, no external dependencies, no server required.

Inspired by [simonw/tools](https://github.com/simonw/tools).

## Conventions

- **One file per tool**: named `tool-name.html` using kebab-case
- **Zero dependencies**: all CSS and JS are inline in the single HTML file
- **Consistent styling**: system font stack (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`), `#f5f5f5` body background, white card container (`max-width: 700px`, `border-radius: 8px`, subtle `box-shadow`), blue accents (`#2563eb`)
- **Responsive**: include viewport meta tag, use `rem` spacing, test at narrow widths
- **Copy button**: every tool with output should have a "Copy" button using `navigator.clipboard.writeText()`
- **Error handling**: show inline red error messages for invalid input
- **No build step**: tools must work by opening the HTML file directly in a browser

## Adding a new tool

1. Create `tool-name.html` in the repo root
2. Follow the structure of `base64.html` as a reference
3. Add an entry to `index.html` in the `<ul>` list:
   ```html
   <li>
       <a href="tool-name.html">Tool Name</a>
       <span class="desc"> — Short description of what it does</span>
   </li>
   ```

## File structure

```
LICENSE          Apache 2.0
index.html       Catalog page listing all tools
base64.html      Base64 Encoder/Decoder
agents.md        This file
```
