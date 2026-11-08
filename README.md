# STGlobe - 3D Population Globe Demo

![Language](https://img.shields.io/github/languages/top/panhavad/stglobe-test-demo) ![Last commit](https://img.shields.io/github/last-commit/panhavad/stglobe-test-demo) [![Release](https://img.shields.io/github/v/release/panhavad/stglobe-test-demo?include_prereleases)](https://github.com/panhavad/stglobe-test-demo/releases/latest)

A single-page **3D globe data-visualization demo** built with [globe.gl](https://github.com/vasturiano/globe.gl) (three.js / WebGL). Countries from a GeoJSON file are drawn on a night-Earth texture and extruded by their estimated population while the globe slowly rotates.

![System snapshot](docs/snapshot.svg)

## Features

- WebGL 3D globe with night-Earth texture
- Country polygons from `dataset.geojson`
- Extrusion height based on population (`POP_EST`)
- Hover labels with country name and ISO code
- Auto-rotation and smooth transitions

## How it works

```mermaid
flowchart LR
    A["index.html"] --> B["globe.gl"]
    A -->|"fetch"| C["dataset.geojson"]
    C --> D["Country polygons"]
    D -->|"altitude = sqrt POP_EST"| B
    B --> E["WebGL 3D globe"]
```

## Getting started

```bash
# any static server works
python -m http.server 8000
# open http://localhost:8000
```

## Download

Grab the packaged source from the [latest release](https://github.com/panhavad/stglobe-test-demo/releases/latest).

## Tech stack

- HTML
- JavaScript
- globe.gl
- three.js
- GeoJSON

## Project structure

```text
stglobe-test-demo/
├── docs/
├── dataset.geojson
├── dataset_original.geojson
├── index.html
└── README.md
```
