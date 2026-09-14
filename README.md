# Anonymous supplementary website

A reading-focused static paper website for GVGNav. Open `index.html` directly in a browser; no dependencies or build step are required. Styling is in `style.css`, and all figures, video posters and videos are in `assets/`. There are no external fonts, scripts, analytics, sidebars or navigation menus. Three compact icon links under the title show Paper, GitHub and Dataset, each marked (coming soon). Videos use native playback controls.

## Publish with GitHub Pages and Anonymous GitHub

1. Create a dedicated GitHub repository for this website. Upload `index.html`, `style.css`, the complete `assets/` folder, `.nojekyll`, `.gitignore`, and this README to its root. Do not upload the parent research project or the local `.tools/` and `.work/` folders.
2. In GitHub, open **Settings → Pages → Build and deployment**. Select **Deploy from a branch**, then `main` and `/(root)`, and save. If your branch has a different name, choose that branch.
3. Wait until GitHub reports that the Pages deployment is live. Check the original page yourself.
4. Open https://anonymous.4open.science/ and sign in with GitHub. Review any requested permissions yourself.
5. Create an anonymization for the repository URL, choose an anonymous identifier, and list identity terms to redact (names, emails, affiliations, account names). Do not redact generic HTML/CSS words.
6. Enable the GitHub Pages option if offered in the anonymization settings. Use the rendered website link provided by the service, not the original GitHub Pages URL and not merely the repository file browser. UI labels may change.
7. Verify the generated anonymous website while signed out. Check every link and future media file. Set expiration after the full review period; avoid redirecting to the original repository during review.

Anonymous GitHub is a mirror, not a tool that makes the original GitHub repository private. The original Pages site is normally public. Account/plan restrictions may affect Pages availability for private repositories.

As checked on 2026-09-14, the service FAQ states that files larger than 8 MB are unsupported, static generators such as Jekyll are not fully supported, and only text files are anonymized. Images, PDFs and videos need manual anonymization. Keep future media below the service limit and verify actual playback through the anonymous URL.

References:
- https://anonymous.4open.science/faq
- https://github.com/tdurieux/anonymous_github
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Current content

- The title, method summary, limitations and result values follow the current `root.tex` manuscript. The manuscript names the method GVGNav.
- Five manuscript figures are included: pipeline overview, trajectory consistency, metric scale recovery, real-robot comparison, and experimental platform.
- Four LTX 2.3 generated rollouts are included: left turn, right turn, box approach, and bin approach. They are explicitly labeled as generated videos rather than physical execution recordings. Descriptions summarize the associated prompts; inclusion does not assert that these examples passed the final validation pipeline.
- Validation results are a selected subset of the manuscript table. Physical-robot results reproduce the manuscript's 12-trial comparison, including its reported 58.4% MASt3R success rate.
- Videos are H.264 MP4, with audio and source metadata removed and fast-start enabled. Original research files are not modified.
- Layout references: https://ei-nav.github.io/NORM-Nav/ and https://finnbusch.com/lotis/ . The page uses an original implementation and does not copy their assets or text.

## Editing

- Edit text in `index.html` and presentation in `style.css`.
- Replace media inside `assets/`, keeping matching relative paths and updating image dimensions and descriptions when needed.
- Keep assets local; do not add identifying repository, profile or media-channel links.
- The `noindex` directive discourages indexing; it does not guarantee anonymity or prevent public access.
- This is a local preview, not yet a deployed anonymous website. Check the eventual anonymous mirror's playback before submission.

## Resource links

In `index.html`, find `data-resource="paper"`, `data-resource="github"`, and `data-resource="dataset"`. Replace each `href="#"` with the real anonymous URL. Remove the corresponding `coming-soon` span and update its `aria-label` when published. Placeholder clicks currently do not navigate or jump to the top; real URLs work automatically.
