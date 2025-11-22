# Chivalry-like Web Prototype

A browser-based prototype aiming for Chivalry 2-style visuals using Three.js. Includes environment-driven PBR lighting, post-processing (SSAO, bloom, SMAA), first-person controls, basic combat, enemies, and a capture objective.

## Features
- Environment-based lighting using an equirectangular image (your uploaded `Chivalry-2.jpg`)
- PBR-ready materials and PMREM environment maps
- EffectComposer: SSAO + Bloom + SMAA
- First-person pointer-lock controls, weapon swing, blocking, stamina, bandages
- GLTF hooks — drop your `.glb` models into `assets/` (see `ASSET_*` in `game.js`)

## Setup
1. Put the project files in a folder (as above).
2. Place your environment image (the screenshot) at the path used in `game.js`. The prototype expects:
   - `/mnt/data/Chivalry-2.jpg` (if your hosting transforms that path)
   or
   - `assets/Chivalry-2.jpg` (if you prefer; update `ENV_IMAGE_PATH` in `game.js` accordingly)
3. Optionally drop GLB/GLTF models into `assets/`:
   - `assets/knight.glb` — enemy model (rigged + animated preferred)
   - `assets/player.glb` — player hands/weapon
   - `assets/house.glb` — building model

## Deploy
- **GitHub Pages**:
  - Create a GitHub repo, push files, go to Settings → Pages → choose `main` branch `/ (root)`, save.
  - Your site will be available at `https://<username>.github.io/<repo>/`.
- **Netlify**:
  - Drag-and-drop the folder into Netlify drop or connect the GitHub repo and deploy.
- **Vercel**:
  - Connect the repo and deploy; select static site settings.

## Notes & Next Steps
To get **very close** to AAA visuals:
- Use high-quality GLB/GLTF models with PBR textures (albedo, normal, roughness, metallic, AO)
- Provide an HDR equirectangular environment (not just a screenshot) for better lighting; Poly Haven has free HDRIs
- Add proper skinned animation clips and play them via `AnimationMixer`
- Add sound SFX and particle VFX for impact
- Tweak postprocessing parameters to taste

If you want, I can:
1. Create the repo ZIP ready for upload.  
2. Integrate specific GLTFs you upload and tune their materials.  
3. Convert your screenshot to a 6-face skybox/HDR-like environment automatically.

Which of those would you like me to do now?
