# shashikumars.github.io

Personal portfolio, served by GitHub Pages at https://shashikumars.github.io.
One static page (`index.html`): no build step, no web fonts, no scripts, no trackers.

## Media

| File | What |
| --- | --- |
| `media/route.webp`, `strength.webp`, `nutrition.webp` | hejje screens, from the hejje website |
| `media/eink-desk.jpg` | The clock in its case, analog face |
| `media/eink-refresh.mp4` + `.jpg` poster | A full colour refresh, 13 s |
| `media/eink-photo.jpg` | Photo-frame mode |
| `media/eink-build.jpg` | The first working build, on jumpers |
| `media/wled.mp4` + `.jpg` poster | LED strips following the monitor, 18 s |
| `media/wled-parts.jpg` | The WLED parts |

How they were made, from the phone originals in `temp/` (kept out of the repo by
`.gitignore`, because they are huge and still carry GPS location):

- Photos: resized to 1600 px wide, JPEG quality 80, drawn into a fresh bitmap so
  no EXIF survives. Checked: 11 GPS tags in each original, none in the copies.
- Videos: re-encoded to 720p H.264 MP4 at 2.5 Mbit/s with no sound, using
  Windows' own MediaTranscoder (`E:\Claude\portfolio-build\transcode.ps1`; this
  machine has no ffmpeg). The WLED clip is seconds 10.5 to 28.5 of the original.
- Posters: one clean frame from each clip (`poster.ps1`), so a visitor downloads
  a video only when pressing play.

## The CV

`cv/Shashi_Kumar_S_CV.pdf` is the main CV (`G:\Jobs\Shashi_Kumar_S_CV.html`)
without the phone number, since this page is public, and with this site's
address added to the header. Regenerate it whenever the main CV changes.

## Link preview and icon

- `og.png` (1200x630) is the card a link to the site shows on LinkedIn, in email and
  in chat. Its source is `_source/og-card.html`; folders starting with `_` are not
  published by GitHub Pages. The render command is at the top of that file.
- `favicon.svg` is the tab icon.
- LinkedIn caches previews. After changing the card, paste the address into
  LinkedIn's Post Inspector (linkedin.com/post-inspector) to refresh it.

## Publishing

1. Create a **public** repository named exactly `shashikumars.github.io`.
2. Push this folder to its `main` branch.
3. GitHub serves it at https://shashikumars.github.io within a minute or two
   (Settings, then Pages, shows the status).

Changes go live with every push to `main`.

## Next

- The e-ink clock code is public at https://github.com/shashikumars/eink-desk-clock
- Add the site's address to the CV header, LinkedIn Featured, every cover letter
  and the outreach email signature.
