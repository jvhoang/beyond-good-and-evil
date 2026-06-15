# Beyond Good and Evil • Graphical Presentations

Full interactive site: https://jvhoang.github.io/beyond-good-and-evil/

This repo hosts the GitHub Pages site for the complete 296-section + Preface + Aftersong graphical summaries and Grok Imagine slide decks (dark academia / minimalist keynote style) of Nietzsche's *Beyond Good and Evil* (Walter Kaufmann translation).

## Current Status (as of push)
- Full dynamic searchable index at root (all 298 entries in JS tocData with links to /sections/XXX.html).
- ~99 section presentation pages populated with:
  - Extensive faithful summary (~400-650 words, key quotes, implications, validation note)
  - 3-5 custom Grok Imagine PowerPoint-style slides with the exact generation prompts shown
  - Consistent dark academic Tailwind design, prev/next nav, back to index (fixed to ../index.html)
- Covers: Preface (000), Sections 1-48 (with some gaps in generation), 62-110. Remaining sections have source .txt but HTML presentations not yet batch-generated.

## Making the links + images work
- **Section links now work**: The many 404s are fixed for the generated sections. Click any card in the index for a full page with content.
- **Images**: The slide <img> tags use relative paths `../images/NN.jpg` (or NN-N.jpg for later batches). These resolve correctly when the images folder lives at the repo root.
  **To complete the visuals (you can do this in 1 minute via GitHub web UI):**
  1. Go to the repo root on GitHub.
  2. Click "Add file" > "Upload files".
  3. Drag in all the .jpg files from your local `bge_analysis/images/` folder (or create an `images/` folder first if needed).
  4. Commit. GitHub Pages will serve them.
- Once images are uploaded, every presentation will display the beautiful custom slides.
- Prompts are always visible below each slide placeholder in the HTML, so the content is educational even before images upload.

## GitHub Pages setup (required for the site and links)
- Repo Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save.
- It may take 30-60s to publish after pushes.
- The index uses absolute https://jvhoang.github.io/beyond-good-and-evil/sections/ links so the GoDaddy embed and direct visits both work.

## For GoDaddy / finalworth.com embed
Use the full single-file index.html (copy from the repo root or the one served at the Pages URL) and paste into a Custom HTML embed. The instructions box inside the index tells you exactly what to do. The section links will open the full presentations on the Pages site in a new tab (or you can adjust).

## Next / Regenerating more sections
Source texts: bge_analysis/sections/*.txt + master_list.json
Full generated data (summaries + prompts): bge_analysis/data/bge_content.json
To add the rest (111-296 + missing gaps): run additional sub-agent batches that read the .txt, write summary + 5 tailored imagine prompts, generate the images via imagine, build the self-contained section HTML, then push via the same process.

## Local assets (for reference)
- bge_analysis/html/*.html (the sources for these pushes)
- bge_analysis/images/*.jpg
- beyond-good-and-evil/index.html (the full dynamic embeddable index)

Educational use only. Enjoy the free spirits.

— Generated and deployed autonomously.