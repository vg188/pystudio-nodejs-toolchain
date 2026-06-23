# PyStudio Node.js Toolchain

Thin build-entry repository for PyStudio Node.js and npm runtime packages.

This repository does not contain a Termux package tree. It calls the reusable
workflow in `vg188/pystudio-termux-builds`, which selects one of the managed
source forks:

- `primary`: `vg188/pystudio-termux-source-termux`
- `secondary`: `vg188/pystudio-termux-source-pacman`

Each run selects exactly one source. Use this repository for the lightweight
Node.js runtime. Native npm build dependencies are built by
`vg188/pystudio-node-build-core-toolchain`.
