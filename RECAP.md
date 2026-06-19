# VariOne site — session recap

Live: **https://varione.ai** (Vercel). Backup mirror: GitHub Pages.
This repo holds the **built** site; the editable source lives separately.

## What was built / changed this session

### Section 3 — Simulator (rebuilt to match the real device)
- Real feature set: Wi-Fi (AP Scan, Deauth, BeaconSpam, VariPortal), Sub-GHz (Capture, Replay, Frequency Scan, RF Jammer, Key Fob Inspect, Load Capture), NFC (EMV Reader, Access Card, Saved Cards), IR (Custom Remote Clone + TV-B-Gone roadmap), **nRF24** (Analyzer, Jammer), **BadUSB**, SD/Files, Mascot.
- **AI-style debriefs** for the attack-class features (VariPortal, Deauth, RF/nRF jammers, BadUSB), with a hand-off from each demo.
- Three buttons: Reset device · View a debrief · Vemo's Academy.

### Section 2 — Meet VariOne
- Updated to match the device (added nRF24 + BadUSB, removed Auth Flood, IR now "working").
- Mobile: animated **accordion** (tap to expand), opaque panels so the background doesn't bleed through.

### Contact form
- Brand modal (name / phone / email / why) → **Web3Forms** → inbox, with honeypot + per-browser rate limiting. Verified delivering.

### Vemo's Academy (companion)
- Pulled in Ahmed's companion app, route renamed **/companion → /vemo**, and its "VariOne" header links back to the landing page.

### Look & feel
- Darker "prestige" palette; pixel arrow + hand cursors (replaced a laggy JS cursor); hero clip tuned to 1080p.

### Mobile / responsive fixes
- Hero height `100svh → 100dvh` (fixes the address-bar seam).
- Layout switches on **touch** (`pointer: coarse`), not just width — zooming out no longer breaks it.
- iOS simulator scroll trap fixed; smaller nav buttons; scroll cue + custom scrollbar hidden on phones; global `overflow-x: clip` guard; tighter mobile spacing.

### Infra / domain
- Production domain set to **varione.ai** (which retired the old `varione-site.vercel.app` URL — expected, not a bug).
- Vercel "Require Log In" (Deployment Protection) turned **off** so the site is public.
- QR code → varione.ai generated as standalone files (kept off the site).
- Footer "Open source on GitHub" link added.

## Open items
1. Add a **Web UI** button in Section 3 (the device's 192.168.4.1 interface) — needs the repo location.
2. Verify the reported mobile "dark strip" (likely persisted browser pinch-zoom; test in phone Incognito).
3. Optional: portrait-cropped hero clip for phones.
4. Publish the editable **source** to its own repo (`varione-site-source`) and add Ahmed as a collaborator — to be done by the owner.
