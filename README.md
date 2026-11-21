# Scan to 3D

Turn any photo into a 3D-printable model, entirely in your browser — no uploads, no server.

**Live:** https://iambangees.github.io/scan-to-3d/

## What it makes

- **Lithophane** — a plate whose thickness follows the photo's brightness (thin = bright). Backlight it and the picture appears. Print upright with a brim, 0.1–0.2 mm layers, 100% infill, light-coloured filament.
- **Relief plate** — the photo as a raised surface on a 1.2 mm base. Print flat, face up.

A single photo cannot reconstruct the hidden back of an object; this tool is honest about that on the page itself. For true object scans you need multi-photo photogrammetry.

## How it works

Photo → brightness grid (detail slider) → height map (lithophane: 0.8 mm at brightest up to the chosen max thickness; relief: brightness × height over the base) → watertight solid mesh (top surface + walls + flat back) → binary STL download. A drag-to-tilt canvas preview and a height-map view show the model before you download. The mesh generator is verified watertight (every edge shared by exactly two triangles).

Everything runs client-side in one static page. Part of the [Bangees](https://github.com/iambangees) family of small tools.
