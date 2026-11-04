# Mist · 薄雾

A frosted, low-contrast theme for [SiYuan](https://b3log.org/siyuan).

![Mist](preview.png)

Mist keeps the interface quiet: no hard panel frames, a translucent frosted sidebar,
soft separators, and a content area that stays readable for hours. Everything is
optional — the theme is complete on its own, and the companion plugin
[**Mist Settings**](https://github.com/dudull852/mist-enhancer) adds a control
panel for tuning it live.

## Real screenshots

Captured from real usage (SiYuan v3.8.9 + Mist 0.2.39), no retouching.

**Database table view** — headers, tags and status columns stay legible under the
low-contrast palette:

![Database table view](assets/01-database-table.png)

**Long-form article** — heading levels, quote blocks, ordered/unordered lists and
links, with line height and weight tuned for long reading sessions:

![Long-form article](assets/02-article-heading-list.png)

**Doc tree hover** — the selected item is a soft blue tint with blue text, and the
hard left bar is gone:

![Doc tree hover](assets/03-article-hover-tree.png)

**Headings mixed with tables** — headings carry extra space above them so sections
read apart, and tables carry their own hairline border:

![Headings mixed with tables](assets/04-doc-heading-table.png)

**Lists and emphasis** — unordered bullets are scaled to 0.7 and dimmed to 30%, so
they no longer compete with the body text:

![Lists and emphasis](assets/05-longform-list.png)

## Highlights

- **No hard frames.** The top bar loses its white strip, the right dock becomes a
  hover-revealed floating strip, the status bar becomes a capsule. The document tree
  and the editor are separated by a drag bar that is invisible but still draggable.
- **Frosted glass.** Floating panels get rounded corners, blur, saturation and a soft
  shadow, on both the left document tree and the right panel.
- **Per-region opacity.** Sidebar, editor, right panel and top bar each have their own
  colour and opacity, so a background image can show through exactly as much as you want.
- **Background image.** Upload your own picture, scoped to the whole window or to the
  editor only, with fill / fit / tile placement.
- **Five one-click palettes.** Mist / Clear / Paper / wolai-like / Night Mist. A palette
  can also carry an accent colour, which is applied to SiYuan's own primary colour so
  buttons, tabs and links change together instead of ending up half-and-half.
- **Typography you can dial in.** Body, doc tree, headings and document title each get
  their own font, size and weight — type a number and see it live (see the caveat below).
- **Table width that fits.** Optionally keep tables within the editor width: overflow
  columns scale down proportionally, and short tables stay narrow instead of stretching.
- **A quieter doc tree.** Each row keeps only a faint **＋** (new sub-document); every
  other action is hidden, including the notebook row's **⋮** — right-click for the rest.
- **Global contrast.** One slider, 0–100: lower pulls text toward the background, higher
  pushes it toward pure black or white. It only moves text, never the background.
- **Light and dark** are two separate designs, not an inverted palette.

## What's new (0.2.38 → 0.2.39)

**Theme**

- Each doc-tree row keeps only a faint **＋** for new sub-documents; all other actions
  are removed (including the notebook row's **⋮**).
- The doc tree's four header buttons (focus / collapse / more / minimise) now appear
  **as a group when the mouse enters the header area**, instead of one at a time.
- Multi-level heading weight unified at **530** (was 600), plus **1.2em** of space above
  headings so sections read apart.
- Tighter spacing between list markers (bullet / number / checkbox) and their text:
  the text block's left indent drops from 34px to 28px.
- Folded list items no longer sprout a stray guide line; block markers are 75% lighter
  than body text and only brighten on hover; unordered bullets are scaled to 0.7 and
  dimmed to 30%.
- Optional table-width adaptation to the editor width (toggle it in the plugin).
- The document info bar (icon / tags / action buttons) **keeps SiYuan's native layout** —
  a horizontal rearrangement was tried, looked wrong in practice, and was reverted.

**Companion plugin (0.2.28 → 0.2.30)**

- New **font-weight controls**: body text, doc tree, multi-level headings and document
  title each get a number (100–900) that applies instantly.
- New **table width adaptation** toggle: never wider than the editor, overflowing
  columns scaled proportionally.
- Font names can be picked from the fonts installed on your machine, or typed by hand;
  separate multiple fonts with commas.

> ⚠️ **Weight doesn't seem to change?** You need a **multi-weight font**. Arial and SimHei
> only have two weights, so 330 and 530 both snap to the same value. Source Han Sans SC,
> Inter, Segoe UI and PingFang SC are variable fonts where 200/400/530/700 are all
> distinguishable. For Chinese text, Source Han Sans SC is a good pick.

## Install

- From the SiYuan marketplace: *Settings → Appearance → Marketplace → Themes*, search
  for `Mist`.
- Manually: unzip `package.zip` into `{workspace}/data/themes/mist/`, then restart SiYuan
  and pick *Mist* under *Settings → Appearance*.

The settings panel shown above comes from the companion plugin
[**Mist Settings**](https://github.com/dudull852/mist-enhancer). Install it from
the marketplace as well; without it the theme still renders fine with its defaults.

## Feedback

Found a bug or have a suggestion? Search **Xiaohongshu (RED)** for account
**`9528590876`** and send a message mentioning "Mist theme + your SiYuan version +
steps to reproduce". I'll get to it as soon as I can.

You can also open a [GitHub issue](https://github.com/dudull852/mist/issues).

## Notes

- The theme is CSS only — no `theme.js`. It does not modify your data.
- Prefer the plugin for tuning. If you would rather not install a plugin, the CSS
  variables in `theme.css` are all documented at the top of the file and can be
  overridden with a code snippet.
- Desktop only (`@media (hover: hover) and (pointer: fine)`); mobile keeps SiYuan's
  native appearance.

## License

MIT
