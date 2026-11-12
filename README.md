# Storm Sailing

Two sailing games in one page, running in the browser.

**Play:** https://icomppower.github.io/saildemo/

## Modes

- **Race the storm** - sail a yacht round four buoys against the clock. The orange dot on the wind dial points to the next buoy, dark patches on the water are gusts, and your best time is saved in the browser.
- **Drift** - take a lantern boat through a flooded, candle-lit hall in the rain. Steer close to the eight dark lanterns to light them and reach the gate at the far end. No clock.

## Controls

- Drag left or right on the water to steer (arrow keys or A/D also work).
- In the race, sliders set rain, wind and wave height.
- **View** cycles the camera, **Sound** turns on rain, wind and sea noise, **Menu** returns to the title screen.

## How it works

Everything is in `index.html`. It uses three.js (r128, loaded from cdnjs) with custom shaders:
layered Gerstner swell plus fine wind chop, sky reflection with Fresnel, crest and wake foam,
rain streaks with ripple rings, and a boat that floats on the same wave function the GPU draws.
The still water in Drift mirrors the scene with a second render pass.
