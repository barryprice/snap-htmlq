# snap-htmlq

**htmlq as a [Snap](https://snapcraft.io) package.**

[htmlq](https://github.com/mgdm/htmlq) is like `jq`, but for HTML — it uses CSS selectors to extract content from HTML files. This repo packages it as a strictly-confined Snap, making it a single-command install on any Linux distribution that supports snaps.

## Install

[![Get it from the Snap Store](https://snapcraft.io/en/dark/install.svg)](https://snapcraft.io/htmlq)

```bash
sudo snap install htmlq
```

## Usage

Pipe HTML through it with a CSS selector:

```bash
curl -s https://example.com | htmlq 'title'
```

```bash
curl -s https://example.com | htmlq --attribute href a
```

See the [upstream README](https://github.com/mgdm/htmlq#usage) for more examples.

## How it works

The Snap wraps a pinned release of htmlq (tracked by Renovate and built with Rust's `cargo`). A CI workflow verifies every push and PR still builds and passes linting, while [snapcraft.io](https://snapcraft.io) handles publishing to the Snap Store on its own schedule.

## Disclaimer

This is a **community-maintained Snap**, not an official mgdm/htmlq project. Issues with the Snap itself should be reported here rather than upstream.

## Credits

- **[mgdm/htmlq](https://github.com/mgdm/htmlq)** — the excellent HTML query tool this Snap packages.
- **[barryprice](https://github.com/barryprice)** — Snap packaging and maintenance.