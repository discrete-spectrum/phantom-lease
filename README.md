# Phantom Lease

Website for the band Phantom Lease (Jacob Trombetta, Brenden Vencel, Mary Riley) —
[phantomlease.com](https://www.phantomlease.com/).

A single static page — no build step, no dependencies.

## Structure

```
index.html      All page content (hero, music, about, contact)
style.css       All styling
images/         Photos, album art, and background patterns
robots.txt      Crawler rules
sitemap.xml     Sitemap for search engines
```

## Running locally

Since it's plain HTML/CSS with no build step, any static file server works. From
the project root:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser.

(A local server is preferred over double-clicking `index.html` — some browsers
restrict how pages loaded via `file://` behave, so serving it over `http://`
matches production more closely.)

Alternatives if you don't have Python:

```bash
npx serve .
```

To stop the server, press `Ctrl+C` in the terminal (or `pkill -f "http.server 8000"`
if it's running in the background).

## Making changes

- **Content** (text, links, album info): edit `index.html` directly.
- **Styling** (colors, layout, spacing): edit `style.css`.
- **Images**: drop new files in `images/` and reference them with a relative path
  (e.g. `images/my-photo.jpg`).

After editing, just refresh the browser — there's no build/compile step.

## Deploying

Upload `index.html`, `style.css`, `robots.txt`, `sitemap.xml`, and the `images/`
folder to the web host, preserving the folder structure (`images/` must stay
alongside `index.html`).
