# SonoAtlasWorld project page

Ready-to-publish static website. No build step, server backend, CDN, model weights,
Python environment or external data mount is required in production.

## Files

```text
index.html          Page with embedded CSS and JavaScript
assets/images/      Paper figures, video poster frames and favicon
assets/videos/      All 13 demo and comparison videos used by this page
.nojekyll           Serve the files directly without Jekyll processing
ASSET_MANIFEST.json File sizes and SHA-256 checksums
README.md           Deployment and editing instructions
```

Only current page assets are included. Paper PDFs, unused demos, training data,
checkpoints, old media and internal QA files are excluded.

## Set the paper link

Both **Read the paper** and **Research paper** currently link to the explicit
placeholder `https://arxiv.org/abs/REPLACE_WITH_ARXIV_ID`.
This is not a real paper URL yet. Replace both occurrences in `index.html` with
the final arXiv abstract URL. Also update the resource subtitle
`arXiv · Link coming soon` when the paper is available.
There is no bundled or embedded paper PDF.

## Deploy to GitHub Pages

1. Create a GitHub repository, for example `SonoAtlasWorld`.
2. Copy the **contents** of this folder into the repository root, preserving the
   `assets/` hierarchy and `.nojekyll`. Do not place this entire folder one level
   below the repository root. Commit and push to `main`.
3. In **Settings → Pages → Build and deployment**, set **Source** to
   **Deploy from a branch**, choose **main** and **/(root)**, then **Save**.
4. The project site will be served at
   `https://YOUR_USERNAME.github.io/SonoAtlasWorld/`.
   A repository named `YOUR_USERNAME.github.io` instead uses
   `https://YOUR_USERNAME.github.io/`.

All media paths are relative, so both root and repository-subdirectory hosting
work. No domain-specific base URL needs to be edited.

Official deployment guide:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Local preview and editing

From this folder, run `python3 -m http.server 8000`, then open
`http://localhost:8000/`. You can also open `index.html` directly.

Edit `index.html` for text, CSS and JavaScript, or replace media while preserving
filenames. The videos are browser-compatible MP4 files and their matching poster
images are in `assets/images/`. The page uses no external fonts or runtime APIs.

The source generator remains in the original workspace at
`output/sonoatlasworld_project/build.py`; after regenerating it, run
`python3 output/sonoatlasworld_project/package_github_pages.py` to refresh this
deployment folder and ZIP. Re-exporting replaces matching files in this folder,
so keep any direct edits in your GitHub repository or apply them to the generator.
