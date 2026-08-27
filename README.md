# sumoapps-legal

Static site serving the landing page and the per-product Support / Privacy / Terms pages for the
**SumoApps** family of Mac apps. ShotSumo is the first product; each future product gets its own
sibling `<product>/` directory with the same three pages, plus one card added to the root
`index.html`'s product list — the landing page itself is not rewritten per product.

## Layout

```
index.html                  SumoApps landing page (product list)
shotsumo/index.html         Support page  → App Store Connect "Support URL" (and optionally "Marketing URL")
shotsumo/privacy.html       Privacy Policy → App Store Connect "Privacy Policy URL"
shotsumo/terms.html         Terms of Use   → linked from the in-app subscription paywall
```

## How it ships

Plain HTML with inline CSS. No Jekyll, no build step, no dependencies. Served by GitHub Pages:
Settings → Pages → Source = `main` / root.

## Relative links

Every link in every page is relative on purpose. A GitHub Pages *project* site is served from
`https://<user>.github.io/<repo>/`, while a *user* site is served from the domain root — which of
the two this repo becomes is not fixed. When editing these pages, never add a leading `/` and
never hardcode a host.

## Content accuracy

Content on these pages must stay truthful to what the shipped app actually does. As of ShotSumo
1.0.0, the app collects nothing, ships no analytics or telemetry, and has no network access at all
(the `com.apple.security.network.client` entitlement is not present in the build). A future paid
version is described on these pages only in clearly-marked future-version sections — never as
something already shipping.
