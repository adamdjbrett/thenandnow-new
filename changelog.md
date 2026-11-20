## 2026-11-19 — Scholarly metadata and feeds

- Identify the site, its digital humanities research project, creator Robert Spiegelman, and sponsor Indigenous Values Initiative in one linked Schema.org graph. The public pages include Zotero citation tags, Dublin Core fields, and IndieWeb entry and author markup.
- Use the apex domain for canonical URLs. Apply the page layout to the privacy and error pages so they also publish metadata.
- Publish Atom at `/feed.xml`, RSS 2.0 at `/feed.rss`, JSON Feed 1.1 at `/feed.json`, and a twtxt timeline at `/twtxt.txt`. The four feeds cover the same three project entries, and each page links to all four formats.
- Publish project credits at `/credits.txt`, refresh the team credits in `/humans.txt`, and point `/robots.txt` to the canonical sitemap. Verify the project identities and feed agreement during the build workflow.

Verified all eight public page heads, three post metadata files, seven output paths, and matching entries in the four feeds. A microformats2 parser extracted the entry titles, URLs and author cards.

## 2026-11-19

- Set the XMIT and HTML referrer policies to `strict-origin-when-cross-origin`. HTTPS requests to Cloudflare Insights carry the site origin while keeping page paths private.
- Allow Cloudflare Insights scripts and requests, YouTube players, and Font Awesome styles, fonts, and kit requests in the public pages’ Content Security Policy.
- Remove the retired Universal Analytics tag and retain the active GA4 measurement tag.
- Pin Ruby 4.0.10 for local builds and CI, and lock Jekyll 4.4.1 with its dependencies for macOS and Linux.

### Verification

The production build passed under Ruby 4.0.10 and Bundler 4.1.0. A Chrome crawl of 10 non-redirect pages found no first-party console errors. All same-site asset paths referenced by the 10 generated HTML files resolved. Chrome and Firefox both received a readable HTTP 200 response from the reported Cloudflare beacon URL.

The 33-second introduction played from the local build in Chrome and Firefox.
