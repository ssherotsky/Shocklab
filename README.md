# Shocklab

**Fork Tuning Lab** is an interactive, animated teaching tool that shows how mountain bike fork suspension works. It is a single self-contained HTML file with no build step.

The goal it teaches: **keep the tire in contact with the ground.** Contact is what gives a rider grip, control and comfort, and a fixed suspension setup can't hold it across changing terrain.

## Run it

Open `index.html` in any modern browser. (Fonts load from Google Fonts; the page works without them.)

## What it shows

A close-up of the front wheel and a 20°-raked fork rolling over a bumpy surface in slow motion. The lower leg slides inside the fixed upper leg, driven by a simple physics model of the wheel, the sprung bike body, the air spring and the damper.

### Controls

- **Terrain:** irregular, washboard or hard bump, with an amplitude slider (25–200%).
- **Variable Terrain:** cycles continuously through all three terrains.
- **Fork tuning:** air pressure, low- and high-speed compression, low- and high-speed rebound.
- **Reset to terrain tune:** loads a good starting tune for the selected terrain.
- **Enable Live Valve:** applies the terrain tune continuously, adapting damping as the terrain changes. Air pressure stays manual.
- **Fork travel:** 120, 140 or 180 mm. Spring rate, sag and bump stop scale with the stroke.
- **Animation speed:** 1x, 2x or 4x for both the animation and the data collection.

### Live monitors

| Monitor | What it measures | Target |
| --- | --- | --- |
| Ground contact | Share of time the tire is touching the ground | 95% or more |
| Travel used | Peak fork compression, as a share of stroke (also shown in mm) | Roughly 30–85%; over 100% is bottoming out |
| Feel | Peak body acceleration relative to the terrain's baseline | Plush or Smooth |

Each monitor has a color-coded running average. **Reset averages** starts a new summary so you can compare combinations of terrain and settings.

## Model notes

- This is a teaching model, not an engineering simulator. Units are drawing pixels (60 px of stroke represents 140 mm), and the ride is a slow-motion replay of a faster one.
- Damping is piecewise: separate low- and high-speed slopes for compression and rebound.
- With a good static tune, Live Valve's gain is modest on a single terrain. Its advantage shows when the terrain keeps changing.

## License

No license has been chosen yet.
