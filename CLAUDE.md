# 11Chem-website

Single-page static landing site. The live page is [index.html](index.html); the original Claude-generated source is preserved as `landing-page (5).html`.

## Stack
- Plain HTML, no build step.
- Tailwind via CDN (`https://cdn.tailwindcss.com`) — fine for prototyping, swap for a built Tailwind bundle before production.
- Google Fonts: Fraunces (display serif), IBM Plex Sans (body), IBM Plex Mono (labels).
- All CSS is inline in a `<style>` block; all SVGs are inline. No external assets.

## Preview
```bash
python3 -m http.server 8040
# → http://localhost:8040
```
Or open `index.html` directly in a browser.

## Conventions
- Edit `index.html` directly. Don't touch `landing-page (5).html` — keep it as a reference snapshot.
- Design tokens (colors, type scale) live in the `:root` CSS variables at the top of the `<style>` block. Change them there, not inline.
- Three Fraunces moments only: hero headline, thesis pull-quote, horizon headline. Everything else is Plex Sans/Mono. Don't add more serif.
- Copper (`--copper: #b85c3c`) is the single accent color — use sparingly.

## Notes
- Folder is named `11Chem-website` but the page content is for "Lattice Bio" — confirm intended branding before publishing.
- Not a git repo yet. Run `git init` if version control is wanted.
- No deployment target configured.
