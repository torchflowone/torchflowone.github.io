# Torchflow.one

Static GitHub Pages landing page for independent Plasma infrastructure. HTML and CSS only; no JavaScript, frameworks, external fonts, tracking, forms or external asset requests.

## Hero: Orbital Observatory

The original user-provided torch shape is preserved in `assets/torch-neon-v2.webp`. It is an optimized encoding of the original PNG, at the same resolution, not a generated redesign of the logo. Five torches are layered above the generated `assets/orbit-observatory-v2.webp` environment. The torches sit lower in the scene, so the orbit intersects the upper handle below the torch bowl, matching the approved position preview. The central reflection follows the lower position; extra scene spacing prevents it from overlapping the caption or page content. A shallow reflection and tiny light glints create depth. The background plate was created with the built-in image generation tool using the original logo palette and banner as references. The two hero assets total approximately 165 KB.

The original source `assets/torch-neon.png` is retained. The 96px favicon is `assets/torch-icon-v2.png`. Assets have new filenames and the stylesheet URL includes a version query to avoid mixing cached old and new visual elements.

Only transforms and opacity animate, on 24–28 second cycles. The `prefers-reduced-motion: reduce` rule disables every animation and transition. The complete scene remains visible when motion is disabled. The scene is decorative and hidden from assistive technology. Keyboard focus outlines, the skip link and forced-colors text fallbacks remain in place.

## Content and security

Public role: **Plasma mainnet observer**, not an active validator. The infrastructure row describes network, node role and operation; it is not a live availability indicator. Existing X, GitHub and email destinations are unchanged. The wordmark is `torchflow.one`.

The previous restrictive CSP is unchanged: scripts, connections, objects, forms and base URLs are disallowed; styles and images are local only. External tabs use `noopener noreferrer`; referrer policy remains `no-referrer`. Meta CSP cannot enforce `frame-ancestors` on GitHub Pages.

## Preview and deployment

Run `python3 -m http.server 8080` from this directory, then open `http://localhost:8080`.

Upload the contents of the update package to the root of the existing main branch: `index.html`, `styles.css`, `README.md` and the `assets` directory. Keep the existing `CNAME` and any `.nojekyll` file. Old, unused image assets do not affect the new page and do not need to be deleted.

Wait for the GitHub Pages deployment to complete, then reload the site. Relative paths work for both the custom domain and a repository subpath.

## Verification — 2026-10-09

- Live HTML was compared with the local baseline before changes; they matched, including the `torchflow.one` wordmark.
- Browser checks at 1440px, 768px, 390px and 320px: no horizontal overflow, images load correctly, existing navigation targets preserved.
- Approved upper-handle orbit alignment checked at 1440px, 768px, 390px and 320px; caption remains clear of following content. Desktop and mobile layouts visually reviewed. Interactive hero links have at least 44px height.
- No browser errors or warnings. Zero script elements. CSP unchanged from baseline.
- Reduced-motion media rule confirmed in the browser's parsed stylesheet; OS-level reduced-motion emulation was unavailable.
- Local preview only; no live deployment was performed for this update.
