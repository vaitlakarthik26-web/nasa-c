# Abandoned but not Forgotten — Space Heritage Museum

A browser-based educational experience about NASA mission hardware and scientific equipment left on the Moon and Mars.

## Project files

- `index.html` — home, interactive planetary archive, Moon and Mars information pages, embedded NASA videos, searchable equipment archive, mission timeline, project information and source links.
- `explore.html` — the existing Three.js first-person field experience, retained and connected to the new navigation. Open with `?world=moon` or `?world=mars` to select a starting environment.

## Run locally

Three.js is loaded as an ES module from jsDelivr, so serve the folder over HTTP rather than opening the HTML files directly from `file://`.

Python:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy to Render

1. Put `index.html`, `explore.html` and this README in the same project root.
2. Push the folder to a GitHub repository.
3. In Render, create a **Static Site** connected to that repository.
4. Set **Build Command** to blank (no build step is required).
5. Set **Publish Directory** to `.`.
6. Deploy. Render will serve `index.html` as the site root; `explore.html` remains available at `/explore.html`.

If the current Render service is a Python web service, create a new Static Site for this frontend or update the existing service only after confirming it is not serving a required backend.

## Controls in 3D EVA

- Desktop: `W A S D` or arrow keys to move, mouse drag to look, `E` to inspect, `Shift` to move faster, `Esc` to close panels.
- Mobile: use the on-screen directional pad and inspect button; drag the scene to look around.

## Important scientific and visual notes

- The 3D planetary textures and field equipment are procedural educational reconstructions, not NASA photogrammetry or engineering-grade replicas.
- HUD coordinates and mission elapsed time are simulated.
- Equipment status labels distinguish items left on a planetary surface, discarded landing components, completed missions and active missions. Active Curiosity and Perseverance are deliberately not described as abandoned.
- Dimensions are approximate where explicitly marked. Refer to the linked NASA mission pages for authoritative mission context.
- NASA YouTube embeds require internet access and may be restricted by the video owner's embedding settings or regional availability.

## Credits and references

NASA: https://www.nasa.gov/  
NASA Image and Video Library: https://images.nasa.gov/  
NASA Moon Science: https://science.nasa.gov/moon/  
NASA Mars Science: https://science.nasa.gov/mars/  

This is an unofficial student educational project and is not affiliated with or endorsed by NASA.
