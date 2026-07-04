# Tort Co Privacy & Security Training

Module 1 is a self-contained interactive course on Encryption & Data Protection. It includes 27 short lessons, practical Tort Co examples, six named workplace scenarios, four human-video placeholders, knowledge checks, a five-question final quiz, saved progress, and a printable completion certificate.

## Deploy with GitHub and Cloudflare

Upload the **contents of this folder** to the top level of the GitHub repository. The repository should show `public`, `.gitignore`, `README.md`, `package.json`, and `wrangler.jsonc` together. Do not upload only the files inside `public`.

In Cloudflare Workers & Pages, connect the GitHub repository. Use these settings:

- Build command: leave blank
- Deploy command: `npx wrangler deploy`
- Root directory: `/`

Cloudflare serves everything in `public` through the Assets setting in `wrangler.jsonc`.

## Add the four recorded videos later

The current course intentionally uses visual placeholders, complete presenter scripts, production notes, and post-video questions. When human recordings are ready:

1. Add the MP4 files to `public/assets`.
2. In `public/app.js`, replace each matching placeholder image block with a `<video controls>` element pointing to the MP4.
3. Add a WebVTT caption file for each recording and include it with a `<track kind="captions">` element.

Recommended filenames: `what-encryption-protects.mp4`, `sharing-data-safely.mp4`, `access-approval-done-right.mp4`, and `reporting-a-security-concern.mp4`.

## Completion tracking

Progress, role, answers, quiz score, and learner name are stored in the learner's browser. The final screen can print or save a certificate as PDF and download a JSON completion record. Organization-wide reporting would require connecting the course to an LMS or database in a later phase.
