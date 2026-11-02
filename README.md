# GhostRev 👻

**Your EV's combustion ghost.** It plays real engine sound for an electric car, driven by your GPS speed. It's made for the Tesla browser.

### ▶ [andiq123.github.io/GhostRev](https://andiq123.github.io/GhostRev/)

| Test drive | GPS mode, parked rev |
|---|---|
| ![Test drive at 4,000 rpm with the cold-engine limit](docs/test-drive.jpg) | ![GPS mode revving in neutral](docs/gps-rev.jpg) |

## How to use

1. In the car, open the link above in the browser and allow location access.
2. Pick an engine and press the power button.
3. Drive. Gears, rpm and exhaust pops follow your real speed, acceleration, hills and corners. While parked, hold the gas pedal to rev.

**Test** mode works anywhere: hold the gas pedal (or ↑ / Space), then let go to hear the pops.

## Features

- **Real recordings:** each engine is a set of seamless loops cut from real recordings at fixed rpm points. The browser's own audio engine plays and crossfades them, so the sound stays smooth even on the car's processor.
- **Three engines:** V8, flat-six and turbo four.
- **Real exhaust crackle:** real recorded overrun crackle when you lift off, and a real bang on full-throttle upshifts.
- **Start-up check:** needle sweep, system checks, starter cranking and a cold fast idle.
- **Warm-up:** a cold engine gets a lower rev limit (the amber arc on the tach), and the coolant temperature is remembered between drives.
- **Smart automatic gearbox:** it learns your driving style, kicks down when you press hard, holds the gear in corners, downshifts for engine braking on hills, ignores GPS noise, and adds rev-match blips, shift lights and a soft limiter.
- **Smooth GPS speed:** a filter made for the Tesla browser's 10 fixes per second without a speed value, so there are no speed jumps, no fake speed while parked, and no gear hunting.
- **Lightweight:** one HTML file and no dependencies. Only the selected car's sounds load (about 250 KB).

## Run locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765. GPS needs HTTPS, so for real driving use the GitHub Pages link.

## Credits

The engine and exhaust sounds come from recordings on [Wikimedia Commons](https://commons.wikimedia.org/) under CC BY 3.0, by Neighborhood Car Reviews, CARSMANIA and FiExhaust. Each file is linked from the ⓘ button in the app. GhostRev isn't affiliated with any car maker.
