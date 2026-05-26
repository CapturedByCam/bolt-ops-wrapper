# Bolt Ops Home Screen Wrapper

Static wrapper for the Bolt Marketing drone operations dashboard.

Current target:

- Client dashboard URL, not operator mode
- Cloudflare Pages custom domain / subdomain for iPhone Home Screen install
- Branded Apple touch icon based on the Bolt enhanced logo asset

Deploy this repository with Cloudflare Pages, Netlify, or Vercel. No build step is required.

## Cloudflare Pages

- Build command: leave blank
- Build output directory: `/`
- Custom domain: `ops.yourdomain.com` or your chosen subdomain

The wrapper serves:

- `/index.html`
- `/manifest.json`
- `/apple-touch-icon.png`
- `/apple-touch-icon-167x167.png`
- `/apple-touch-icon-152x152.png`
- `/icon-192.png`
- `/icon-512.png`
- `/icon-source.png`

Add the custom-domain URL to the iPhone Home Screen, not the Apps Script URL.

## Current Notes

- The wrapper now points at the client dashboard deployment.
- iPhone standalone mode still appears to reserve a bottom inset when the Apps Script app is embedded cross-origin in an iframe.
- The remaining bottom slab looks iOS-side rather than a missing CSS rule in the wrapper.
- If needed later, the next escalation path is replacing the iframe wrapper with a redirect launcher.
