# heartlog-public-pages

Public site for [Heartlog](https://apps.apple.com/us/app/heartlog-dating-journal/id6757116727), the dating journal for iPhone. Landing page, changelog, support, Privacy Policy, and Terms of Service. Served by GitHub Pages from the `main` branch root.

## Live URLs

- Home: <https://trevornogues.github.io/heartlog-public-pages/>
- Changelog: <https://trevornogues.github.io/heartlog-public-pages/changelog/>
- Support: <https://trevornogues.github.io/heartlog-public-pages/support.html>
- Privacy Policy: <https://trevornogues.github.io/heartlog-public-pages/privacy-policy.html>
- Terms of Service: <https://trevornogues.github.io/heartlog-public-pages/terms-of-service.html>

The support, privacy, and terms URLs are the ones registered in App Store Connect. Keep those filenames stable.

## Structure

```
.
├── index.html                 # Landing page (storefront)
├── changelog/index.html       # Release notes, newest first
├── support.html               # Support and FAQ
├── privacy-policy.html        # Privacy Policy
├── terms-of-service.html      # Terms of Service
├── styles.css                 # Shared styles (brand tokens at the top)
├── assets/
│   ├── icon.png, favicon.png, og-image.jpg
│   └── screens/*.jpg          # 640x1056 app screenshots for the landing page
├── robots.txt, sitemap.xml, llms.txt
└── .nojekyll
```

## Editing

Plain HTML and CSS, no build step. Edit, commit, push to `main`; Pages redeploys in a minute or two.

- Legal pages: bump the `Last updated` line when the text changes.
- After a release: add an entry to `changelog/index.html`, update `softwareVersion` and `dateModified` in the JSON-LD on `index.html`, and bump `lastmod` in `sitemap.xml`.
- After new reviews land: refresh the rating line in the hero and `ratingCount` in the JSON-LD.
- Prices are stated on `index.html`, `llms.txt`, and in the JSON-LD. Keep all three in sync with App Store Connect.

## Keeping the landing page honest

Only claim what the app does today and what the App Store listing says. No testimonials until real ones are collected (there is a commented-out block in `index.html` ready for them). Do not use em dashes in copy.
