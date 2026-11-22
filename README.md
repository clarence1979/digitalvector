# Digital Vector

Source for https://digitalvector.com.au, served by GitHub Pages from the `main` branch.

- `index.html` is the page: content, forms and the script that drives the 3D walk-in.
- `assets/` holds everything the 3D view loads:
  - `school.glb`: the school, corridor and computer lab, modelled in Blender (geometry compressed with meshopt).
  - `lm_*.webp`: baked lighting (Cycles) for each part of the model. Files ending `_s` are the smaller set phones load.
  - `scr_*.jpg`: what the lab's screens show, including the four About slides on the wall display.
  - `poster.jpg`, `poster-m.jpg`: still images shown while the model loads, or if a browser has no WebGL.
  - `three.min.js`, `GLTFLoader.js`, `meshopt_decoder.js`: three.js r128 and its loader, kept here so nothing depends on a CDN.
- `CNAME` tells GitHub Pages the custom domain. Do not delete it.
- The "Join the list" form writes to the `newsletter_signups` table in Supabase (insert only).

The Blender scene, the Python scripts that build and bake it, and the texture sources are kept outside this repository
(on the owner's computer, in `Documents\Digital Vector Website\3d`). To change the model, edit those scripts, re-run the
bake, and replace the files in `assets/`.

Last republished: 22 November 2026.
