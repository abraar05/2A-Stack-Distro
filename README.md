# 2A_Stack

Wholesale ERP — orders, inventory, purchasing, customers, finance and insights with an embedded local-AI copilot.

Part of the **Nexus suite** — five interconnected but independent workspaces, each a self-contained static web app (no build step, no framework, no runtime dependencies):

- [2A_Stack](https://abraar05.github.io/2A_Stack/) — Wholesale ERP
- [2A_Stack People](https://abraar05.github.io/2A_Stack People/) — People & Admin
- [2A_Stack Logistics](https://abraar05.github.io/2A_Stack Logistics/) — Logistics Control Tower
- [2A_Stack Portal](https://abraar05.github.io/2A_Stack Portal/) — Customer Portal
- [2A_Stack CRM](https://abraar05.github.io/2A_Stack CRM/) — CRM

Each app links to the others via the **Nexus suite** section in its sidebar, but they are separate products, separately deployed, separately versioned.

## Structure

```
index.html            app shell
css/app.css           design tokens + components
js/config.js          app metadata, suite links, module pages
js/app.js             router, themes, AI drawer, toasts, SW registration
sw.js                 offline cache (service worker)
manifest.webmanifest  PWA manifest
icon.svg              app icon
```

## Run locally

```sh
npm start          # python3 http.server on port 8801
# or
npm run serve      # npx http-server on port 8801
npm run check      # syntax-check the JS
```

## Deploy (GitHub Pages)

1. Create a new repo named `2A_Stack` and push this folder.
2. In the repo: **Settings → Pages → Source: GitHub Actions**.
3. The included `.github/workflows/pages.yml` deploys on every push to `main`.

Site URL: `https://abraar05.github.io/2A_Stack/`
