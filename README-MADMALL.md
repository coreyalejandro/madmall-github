# MADMall — drop-in for zmux-design-system

Unzip this at the ROOT of your `zmux-design-system` clone. It adds:

    app/mall/page.tsx          # MADMall — image-led rooms (server component)
    app/mall/SafetyLayer.tsx   # real ZMUX safety components (client island)
    public/madmall/*.jpeg      # the 8 room images (served at /madmall/...)

The page references images by local path (e.g. /madmall/sanctuary.jpeg), so
nothing depends on temporary URLs.

## Commit & push

    git checkout -b madmall-phase-3
    git add app/mall/page.tsx app/mall/SafetyLayer.tsx public/madmall
    git commit -m "Add MADMall: image-led rooms + real ZMUX safety layer"
    git push -u origin madmall-phase-3

Then open the PR link GitHub prints and merge after review.

## Image -> room mapping
    sanctuary.jpeg -> hero/atrium   apparell.jpeg -> retail
    jazz.jpeg -> jazz               comedy.jpeg   -> comedy
    wellness.jpeg -> wellness       learning.jpeg -> learning
    commons.jpeg -> commons         care.jpeg     -> care

## Notes
- Visit /mall after `npm run dev`.
- Keep your existing app/layout.tsx (Space Grotesk via next/font) — not included here.
- Images are ~3 MB each (~24 MB total). Consider compressing or Git LFS later.
