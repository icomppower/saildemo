# Storm Sailing

A real-time sailing demo that runs in the browser: steer a yacht across a rainy sea.

**Live demo:** https://icomppower.github.io/saildemo/

## Controls

- Drag left or right on the water to steer (arrow keys or A/D also work).
- Sliders set rain, wind and wave height.
- **View** cycles between astern, leeward rail and masthead cameras.
- **Sound** turns on rain, wind and sea noise.

## How it works

Everything is in `index.html`. It uses three.js (r128, loaded from cdnjs) with custom shaders:
layered Gerstner swell plus fine wind chop for the water, sky reflection with Fresnel,
crest and wake foam, rain streaks with ripple rings on the surface, and a boat that floats
on the same wave function the GPU draws.
