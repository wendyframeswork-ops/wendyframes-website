# WendyFrames static website (starter)

## Setup
1. Upload the contents of this folder to the root of your GitHub repository. **Include `.pages.yml`** (hidden file).
2. In Cloudflare Pages, connect the repository. Framework preset: None; build command: `exit 0` (or leave blank); output directory: `/` or `.` as the UI permits.
3. Open https://app.pagescms.org and authorize the repository.
4. Update text/images in the CMS. Upload real photos before promoting the site.

## IMPORTANT: project index limitation
This first version uses `content/projects.json` as a manifest of project filenames. When you **add or delete** a project through Pages CMS, you must also update this manifest in GitHub; otherwise the project will not appear/disappear. Editing photos and details of existing projects does not require this step. This can be improved with a static-site build step later.

## Test
The site uses `fetch()` to load JSON. Do NOT open `index.html` directly using a `file://` URL; test using a local HTTP server (`python -m http.server 8000`) or the deployed site.

## Caveats
- This is a starter conversion of the draft, not a production-tested CMS integration. Verify the Pages CMS configuration after connecting; their schema can change.
- Replace all placeholder images and review copy/contact links before launch.
- Cloudflare Pages will serve the HTML and JSON files; updates to existing content are deployed after a GitHub commit.
- Uploaded assets should be optimized for web; large photos increase repository size and page load times.
- HTML with JS-fetched content has SEO limitations. A later static build would improve indexability.
