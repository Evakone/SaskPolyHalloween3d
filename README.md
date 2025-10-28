# Sask Polytech Halloween AR — WebXR

Single-page WebXR experience built with `<model-viewer>` for the Sask Polytech Halloween signage demo. No A-Frame, AR.js, or MindAR.

## Structure

```
SaskPolyHalloween3d/
├── index.html                               # Model preview + AR (single page, Sask Polytech branding)
├── vercel.json                              # Asset headers + rewrite
├── 3D-Model-Demo-Halloween-clean-opt.glb    # Primary WebXR asset
├── SaskPolytech_small_web.png               # Header logo art
└── textures/                                # Additional baked textures (optional)
```

## Steps

1) Replace or update `3D-Model-Demo-Halloween-clean-opt.glb` with your latest GLB export (animations supported).
2) (Optional, for iOS Quick Look) Generate a matching `3D-Model-Demo-Halloween.usdz` and add it to the project root, then re-enable the `ios-src` attribute in `index.html`.
3) Open `index.html` locally, or deploy to Vercel.

## Notes

- Animations: the GLB’s clips auto-play with loop + sequencing logic.
- AR transparency: CSS avoids forcing a solid background once AR starts, so AR viewers show through correctly.
- Vercel config sets MIME for `.glb` under `/assets/`.
