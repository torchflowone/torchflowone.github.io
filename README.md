# Torch Flow One

Static GitHub Pages landing page for independent Plasma infrastructure. HTML and CSS only: no JavaScript, frameworks, external fonts, tracking, forms or external asset requests.

## Branding

The original user-provided neon torch is preserved in `assets/torch-neon.png`. The banner reference is translated into a CSS orbit scene rather than used as a page background. Four subdued copies of the torch surround the central mark. CSS masks and screen blending integrate the original dark image background; the source image is unmodified.

Animation uses only opacity and transforms, with 24–28 second cycles. `prefers-reduced-motion: reduce` disables every animation and transition. The orbit scene is decorative and hidden from assistive technology. The page includes keyboard focus outlines, a skip link, and a forced-colors fallback for gradient text.

## Content

Public role: **Plasma mainnet observer**, not an active validator. The infrastructure row describes the network, role and operation; it is not a live availability indicator. No uptime, monitoring, delegation or validator claims are made.

Existing links are preserved: X `https://x.com/torchflowone`, GitHub `https://github.com/torchflowone`, contact `hello@torchflow.one`.

## Preview and deployment

Run `python3 -m http.server 8080` from this directory. Open `http://localhost:8080`.

The existing `.nojekyll` and `CNAME` are unchanged. Deploy the root of this repository through its existing GitHub Pages configuration. Relative asset paths also work under a project path.

## Security

The existing restrictive CSP is unchanged: scripts, connections, objects, forms and base URLs are disallowed; styles and images are local only. External tabs use `noopener noreferrer`; referrer policy remains `no-referrer`. GitHub Pages does not provide arbitrary security response headers; meta CSP cannot enforce `frame-ancestors`.

## Redesign verification

Visually reviewed in the Codex browser at 1440px desktop and 390px mobile. Checked 320px mobile for horizontal overflow and image loading. Navigation destinations match the previous version; no browser errors or warnings were observed. Reduced-motion rules were inspected in the stylesheet (browser motion emulation was unavailable).
