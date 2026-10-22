# Fabian Ramírez — Portfolio

[![CI](https://github.com/FyrmzDevMx/portafolio-fabian/actions/workflows/ci.yml/badge.svg)](https://github.com/FyrmzDevMx/portafolio-fabian/actions/workflows/ci.yml)

Personal portfolio and project showcase for [fyramirez.dev](https://fyramirez.dev). The site presents selected work, experience, and skills in Spanish and English.

## Local activation service

The Node.js service supports the portfolio's activation flow and listens on `127.0.0.1:4181` by default.

Requirements: Node.js 22 or later.

```sh
node server.mjs
```

The local endpoint is available at `http://127.0.0.1:4181/api/activate`. To expose it temporarily for the live site, see [README-local-tunnel.md](README-local-tunnel.md). Do not store Cloudflare credentials or other secrets in this repository.

## Checks

Run the activation tests and JavaScript syntax checks with:

```sh
node --test server/activation.test.mjs
node --check server.mjs
node --check server/activation.mjs
node --check activation.js
node --check i18n.js
```

These are also run by the GitHub Actions workflow on pushes and pull requests.

## Repository layout

- `index.html`, `style.css`, and `portfolio-assets/`: portfolio entry page and front-end assets
- `i18n.js`: language and route support
- `server.mjs` and `server/`: local activation service and tests
- `README-local-tunnel.md`: optional temporary tunnel setup
