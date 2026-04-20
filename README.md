# Red Tide Data Reanalysis

Senior capstone project: ensemble-based reanalysis of Peace River hydrology inputs to a Karenia brevis bloom prediction model.


## Contents

This repository contains the source for a Jupyter Book presenting two parallel analyses:

- **Discharge** — reanalysis of Peace River discharge at USGS Station 02296750
- **Total Nitrogen** — reanalysis of TN loading at the same station

Each track applies four uncertainty quantification methods: Bootstrap, GLUE, EnKF, and LPU.

## Building locally

```bash
pip install -r requirements.txt
jupyter-book build .
```

The built site lands in `_build/html/`. Open `_build/html/index.html` in a browser to preview.

## Deploying

The book is published to GitHub Pages. See `.github/workflows/deploy.yml` (if configured) or deploy manually with:

```bash
pip install ghp-import
ghp-import -n -p -f _build/html
```

## Source

Notebooks in this repository are pre-executed snapshots.