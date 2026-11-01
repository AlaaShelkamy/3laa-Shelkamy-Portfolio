# 3laa Shelkamy — Portfolio V4

A bilingual (English / Arabic) static portfolio built for GitHub Pages. This release builds on V3; it retains the hero, existing visual identity, typography, contact links and 4 green signature labels.

## What changed in V4

- Featured Collaborations section immediately below the hero, with a creator profile card, verified-status label, portrait sourced from the screenshot supplied by the portfolio owner, follower count shown as **3.9M**, bilingual project-vision copy, Instagram profile button and a 2-video next/previous switcher.
- `Work` and `Explore My Work` (and their Arabic equivalents) scroll to `#featured`.
- Selected Work now has All / Celebrities / Motion Graphics / Medical filters, and independent horizontally swipable carousels, scroll-snap, buttons and opacity fades on the edges.
- About section's Premiere Pro, After Effects and DaVinci Resolve skill chips feature small matching app marks and a soft full-chip blue glow.
- Five distinct Vimeo projects are listed. The two creator films are reused in the Featured section and the Celebrities category.
- Vimeo embeds load only after the viewer presses Play, and other open players are removed automatically.

## Vimeo videos

| Project | Vimeo ID | Category | Aspect ratio |
| --- | --- | --- | --- |
| Aloosh Alameer 01 | 1242108707 | Celebrities | 9:16 |
| Aloosh Alameer 02 | 1242108886 | Celebrities | 9:16 |
| Real Estate Voiceover — Yemen | 1242111864 | Motion Graphics & Voiceover | 9:16 |
| Medical Reel — Haya | 1241990617 | Medical | 9:16 |
| Medical Reel — E.N.A.N.A Iraq | 1241984622 | Medical | 9:16 |

## Files

- `index.html`: all markup, styling, translation strings and behavior (no build step)
- `assets/portrait.webp`: original portfolio photo from V3
- `assets/aloosh-profile.webp`: cropped profile photo from user-provided Instagram screenshot
- `assets/fonts/Palestine-Regular.woff2` and `.ttf`: locally hosted Arabic font

The English IBM Plex Sans and Press Start 2P fonts are loaded from Google Fonts and need internet access. Profile links and social/contact links are already configured.

## Deployment to GitHub Pages

1. Extract the ZIP.
2. In the `3laa-Shelkamy-Portfolio` GitHub repository, replace the existing `index.html` and upload the `assets` folder contents, including the new Aloosh profile photo.
3. Ensure `index.html` stays at the repository root and `assets/` is next to it, not nested in a second parent directory.
4. Commit changes and hard-refresh the published GitHub Pages page after deployment.

**Important:** This ZIP is a website source artifact; the actual GitHub site is not updated until you deploy it.

## Editing projects later

In `index.html`, project cards are in `#work` under `.project-group` sections. The carousel JavaScript works with arbitrary numbers of `.carousel-card` children. For new Vimeo projects, duplicate one `.work-card`, set its `.video-frame` `data-video-id` and `data-video-name`, update its poster/title, and adjust the `.carousel-count` total. No external backend is required.

## Verification

Checked page script syntax and browser interactions on 1440px desktop, 390px mobile and 320px compact mobile, in both Arabic and English. Tested category filtering, featured arrows, horizontal carousel navigation and disabled end arrows. No horizontal document overflow or JavaScript page errors in those checks. External Vimeo playback was not tested against Vimeo's live service during offline browser verification.
