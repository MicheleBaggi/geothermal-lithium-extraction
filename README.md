# Fracture Networks in Geothermal Energy & Lithium Co-Production

A reveal.js presentation analyzing the simulation study by **Banshoya, Berre & Keilegavlen (2025)** on the impact of fracture networks on geothermal energy and lithium co-production from subsurface brines.

Prepared for the course *Numerical Methods for the Geosciences* — January 2026.

## Live presentation

[View the slides on GitHub Pages](https://michelebaggi.github.io/geothermal-lithium-extraction/)

> To enable GitHub Pages: go to **Settings → Pages → Source**, select branch `master`, folder `/ (root)`, and save.

## What this presentation covers

The study models a geothermal doublet system (one injection well, one production well) in a fractured porous medium, tracking three coupled physical processes simultaneously:

- **Flow** — single-phase Darcy flow through matrix and fractures
- **Lithium transport** — advection of Li concentration (no diffusion)
- **Heat transfer** — convection + conduction with local thermal equilibrium

The key finding: **fracture connectivity dominates lithium recovery**, while energy output remains relatively stable thanks to thermal diffusion. A well-connected fracture pathway between wells causes early lithium breakthrough (short-circuiting), while a disconnected network buffers the Li front. Thermal breakthrough is always delayed relative to chemical breakthrough.

The model uses a mixed-dimensional framework (PorePy) where fractures are represented as lower-dimensional manifolds coupled to the 3D/2D matrix — avoiding expensive 3D fracture meshing while preserving the physics.

## Reference article

> Banshoya, K., Berre, I., & Keilegavlen, E. (2025).
> *A simulation study of the impact of fracture networks on geothermal energy and lithium co-production.*
> **Geothermal Energy.**

The full PDF is available in the [Releases](https://github.com/MicheleBaggi/geothermal-lithium-extraction/releases) section.

## Running locally

```bash
npm install
npm start
```

Then open `http://localhost:8000` in your browser.

## Built with

- [reveal.js](https://revealjs.com/) — HTML presentation framework
- [KaTeX](https://katex.org/) — math rendering
- [PorePy](https://github.com/pmgbergen/porepy) — mixed-dimensional simulation framework (used in the referenced study)
