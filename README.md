<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./plainsight-labs-logo-dark.svg" />
    <img src="./plainsight-labs-logo.svg" alt="PlainSight Labs" width="160" />
  </picture>
</p>

# hugo-theme-aperture

A neutral, documentation-forward Hugo theme intended for institutional governance sites. The theme is designed to be brand-capable without brand defaults. All visual decisions are expressed as semantic CSS tokens and can be overridden at the site level.

## Install

1. Add the theme as a git submodule:

```bash
git submodule add <repo-url> themes/hugo-theme-aperture
```

2. Reference it in your site config:

```toml
theme = "hugo-theme-aperture"
```

## Use

Run the example site locally:

```bash
cd exampleSite
hugo server
```

## Override Tokens (CSS Variables)

All design decisions are expressed in `:root` tokens in `assets/css/main.css`. Override them from your site by adding a custom stylesheet and loading it after the theme stylesheet.

Example override file `assets/css/overrides.css`:

```css
:root {
  --color-bg: #ffffff;
  --color-fg: #111111;
  --color-accent: #2f6f8f;
  --font-sans: "Inter", system-ui, -apple-system, "Segoe UI", sans-serif;
}
```

Then reference it from your site config:

```toml
[params]
  customCSS = ["css/overrides.css"]
```

## Override Partials

Partials live in `layouts/partials/`. To override, copy a partial into your site with the same relative path, for example:

- `layouts/partials/header.html`
- `layouts/partials/footer.html`
- `layouts/partials/head.html`

Hugo will prefer the site-level version over the theme version.

## Callouts

Use the `callout` shortcode for inline, wide, or full-bleed callouts. `wide=true` breaks out beyond the reading column while staying centered and bounded. `bleed=true` spans the viewport background while keeping inner content constrained. No JavaScript is required, and appearance is driven by CSS tokens.

```md
{{< callout type="note" title="Note" >}}
Normal callout within reading column.
{{< /callout >}}

{{< callout type="warning" title="Warning" wide="true" >}}
Wide callout (breakout) to emphasize a boundary condition.
{{< /callout >}}

{{< callout type="danger" title="Critical" bleed="true" >}}
Full-bleed callout (viewport background), but content text remains constrained.
{{< /callout >}}
```

## Branding

This theme intentionally ships with no logos, taglines, or brand-specific colors. Branding belongs at the site layer through overrides.

## Licensing

This repository is MIT licensed for code and documentation, with an explicit asset exception for
`plainsight-labs-logo.svg` and `plainsight-labs-logo-dark.svg`, which are copyrighted and not covered
by the MIT license. See `LICENSE` for details.
