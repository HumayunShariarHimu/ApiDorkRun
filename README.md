# ApiDorkRun

A mobile-first static API discovery and manual request workbench for authorized security research.

## Features

### Search / dork workflow
- Responsive phone, tablet, and desktop layout.
- Six category-specific query packs: Core API JSON, Swagger/OpenAPI, Configuration Exposure, GraphQL, Admin/Internal Paths, and Code/Paste.
- Load a selected category, append all packs, or restore defaults.
- Import .txt query lists (2 MB maximum), edit queries, clear/reset, copy, and export.
- Optional target-domain scoping, validated delay and query limit.
- Prepare, preview, copy, and export Google search URLs.
- Open individual URLs or all prepared URLs; cancellable launch queue, dry-run mode, progress, and browser-launch toggle.
- Bookmarklet helper, accessible status announcements, keyboard focus, and reduced-motion support.

### Manual API request workbench
- Import local OpenAPI 3.x or Swagger 2.0 JSON files (2 MB maximum).
- Select supported HTTP operations, edit URL/method/headers/body, and send one confirmed request at a time.
- 15-second timeout; display HTTP status, duration, response size, readable headers, and response body (display capped at 1 MB).
- Browser credentials are omitted by default. No server, telemetry, or browser storage is used.

## Limitations and safe use
- This is not an automated vulnerability scanner. It does not fuzz, exploit, brute-force, or automatically crawl endpoints.
- Browser CORS, TLS, network, and private-network rules can block requests or hide response headers. A failed browser request does not prove an endpoint is down.
- Import JSON only; YAML is not supported. Replace generated path placeholders and review every request before sending.
- Search results depend on Google and may be incomplete. Popup blockers can prevent multiple tabs.
- Use only systems and data you own or are explicitly authorized to test. Prefer test environments for non-read-only methods; never send destructive requests to production without authorization.

## Run locally
Open index.html in a modern browser or serve the folder:

    python -m http.server 8000

Then visit http://localhost:8000/.

## GitHub Pages deployment
The workflow .github/workflows/pages.yml publishes index.html whenever a commit reaches main, or when manually started from Actions. In repository Settings > Pages, choose GitHub Actions as the deployment source if needed. The first deployment may take a few minutes.
