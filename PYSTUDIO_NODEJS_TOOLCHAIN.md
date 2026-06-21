# PyStudio Node.js toolchain

Source: `msmt2018/termux-packages`

This repository builds the Node.js toolchain packages for PyStudio:

- Android package: `com.vchangxiao.pystudio`
- Prefix: `/data/data/com.vchangxiao.pystudio/files/usr`
- Package format: Debian `.deb`

The default workflow builds `aarch64` packages for:

- `nodejs`
- `npm`

Dependencies are built from source instead of downloaded from the official
Termux repositories, so the generated packages keep the PyStudio prefix.

The workflow publishes raw `.deb` files and a minimal apt repository archive
with `Packages`, `Packages.gz`, and `Packages.xz` indexes.

Python and C/C++ toolchains are built in separate repositories so PyStudio can
install only the toolchain a project actually needs.
