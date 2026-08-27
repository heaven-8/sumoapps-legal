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
