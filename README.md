# Wellness Eras Lead Magnet Landing Page

This version is intentionally focused on one primary action: getting the visitor to request the free 7 Day Clean Eating Plan.

## What changed

- Larger, stronger hero
- Clearer value proposition
- Much larger food visual
- Sender form remains integrated
- 28 Day Plan navigation and page are intentionally removed from this lead magnet
- Three concise benefit cards
- Short food preview section
- One final CTA
- Minimal footer
- Separate editable logo asset
- Separate editable food assets
- Responsive layout

## Sender integration

The Sender universal script from the supplied website has been preserved.

Sender account initialization:
`sender('952dde70111419')`

Sender form:
`data-sender-form-id="bmZ39R"`

Do not remove either unless you intentionally change your Sender setup.

## Change the logo

Replace:
`assets/logo-mark.svg`

The same file is used in the header, footer, and favicon.

## Change the hero image

Replace:
`images/hero-food.svg`

The hero is intentionally controlled by one simple image element in `index.html`.

For the strongest production result, replace the included artwork with a high quality, realistic food photograph. Recommended: a square or slightly vertical top-down photograph showing eggs, avocado, greens, tomatoes, grilled chicken or another colorful clean eating meal.

If you replace the SVG with a JPG, for example `images/hero-food.jpg`, update the `src` in `index.html`.

## Change the second food image

Replace:
`images/meal-preview.svg`

## Deploy

Upload the ZIP contents to the root of your GitHub repository. No build process is required.

If using GitHub Pages, configure the repository's Pages settings and custom domain there.

## Important

The privacy and terms pages are starter copy, not legal advice. Review them for your actual business, jurisdiction, email practices, consent wording, analytics, and other services before publishing.
