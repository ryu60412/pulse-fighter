# Pulse Architect v2 — with Sound 🎵

🎮 **Play it now:** Open `index.html` in your browser, or deploy to GitHub Pages.

A browser-based **roguelike** game where you **design the waveform** of your attacks in real-time.
Adjust Capacitance (Cap), Resistance (R), Pulse width, and Noise — each parameter affects your damage,
fire rate, critical chance, and accuracy.

**v2 adds full Web Audio API sound design — no external sound files required!**

---

## 🎯 Concept

Inspired by the world of semiconductor pulse design, **Pulse Architect** turns electrical-circuit
intuition into a game. Sliders aren't just stats — they reshape the actual waveform of your shots
*and* the sound of your gun.

- **High Cap** → Bigger pulses, slower fire rate, lower-pitched shots
- **High R** → More stable, slightly less damage
- **High Pulse** → Longer-lasting shots, higher-pitched sound
- **High Noise** → Higher crit chance, but lower accuracy

Find your build. Discover synergies. Survive deeper.

---

## 🎵 Sound Features (NEW in v2)

All sound is **synthesized in real time** using the Web Audio API.
No MP3 or WAV files — just pure code-generated audio.

### SFX
| Event | Sound |
|---|---|
| Shoot | Square-wave chirp (pitch follows Pulse, length follows Cap) |
| Hit | Filtered noise + low sawtooth thump |
| Crit | Bright two-tone square-wave chime |
| Kill | Noise burst + descending sawtooth sweep |
| Damage | Low square + filtered noise |
| Upgrade select | Two-note sine arpeggio |
| Floor clear | C–E–G–C triangle-wave arpeggio |
| Game over | Three descending sawtooth notes |

### BGM
- Synthesized loop with **lead saw + triangle bass + hi-hat noise**
- Am pentatonic mood
- Auto-starts on game start, auto-fades on game over

### Volume Controls
- Top-right volume slider
- 🔊/🔇 mute toggle

---

## 🎮 Controls

| Key | Action |
|---|---|
| `W` `A` `S` `D` | Move |
| `Mouse` | Aim |
| `Left Click` | Shoot (hold to auto-fire) |
| `Sliders (bottom)` | Design your attack waveform |
| `Top-right volume` | Master volume |
| `🔊 button` | Mute/Unmute |

After each floor, choose **one of three upgrades** to power up your build.

---

## 🚀 How to Deploy to GitHub Pages

1. Create a new GitHub repository (e.g., `pulse-architect`)
2. Upload `index.html` to the root
3. Go to **Settings → Pages**
4. Under **Source**, select `main` branch and `/ (root)`
5. Click **Save**
6. Your game will be live at:
   `https://<your-username>.github.io/pulse-architect/`

No build step. No dependencies. No sound files.

---

## 🧪 Run Locally

Just open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).

Or serve with any static server:
```bash
python3 -m http.server 8000
# Then open http://localhost:8000
```

> ⚠ **Note**: Browsers block audio until user interaction.
> Sound will start when you click the **START** button. This is by design.

---

## 🛠 Tech

- Pure HTML5 Canvas + vanilla JavaScript
- **Web Audio API** for all sound (no external files)
- Single self-contained file
- ~900 lines of code
- 60 FPS target

---

## 📋 Features

### Gameplay
- [x] Real-time waveform-based combat
- [x] Oscilloscope-style visualization
- [x] Procedural floor progression
- [x] 3-card upgrade selection
- [x] Common / Epic rarity tiers
- [x] Enemy HP/damage scaling per floor (×1.18 / ×1.12)
- [x] Crit / accuracy / fire-rate from waveform
- [x] Particle effects & damage numbers

### Audio (NEW)
- [x] Synthesized SFX (8 distinct sounds)
- [x] Synthesized BGM loop
- [x] Volume control + mute
- [x] Shoot sound follows waveform parameters
- [x] Dynamic compressor (no clipping)
- [x] Max simultaneous nodes capped at 30

### Planned (Future)
- [ ] Stereo panning (enemy direction)
- [ ] Reverb for explosions
- [ ] More modules (30 designed)
- [ ] Circuit chips (40 designed)
- [ ] Synergy system
- [ ] Boss fights with waveform interference
- [ ] Persistent meta-progression (research lab)

---

## 📄 License

MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
