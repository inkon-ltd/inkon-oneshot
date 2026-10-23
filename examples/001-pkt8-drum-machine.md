# PKT-8: one-shot prompt (example)

> Idea: "can you build me a [compact drum machine] as an html app to create dance music and loops?"

This was the **first ever One Shot**. Built the normal way, it took four prompts:
1. the drum machine,
2. "it needs a reset button",
3. "give me house styles, a button to swap each instrument, make it a generator",
4. "make a 9:16 filming mode".

The prompt below is what `/oneshot` writes for that same one-line idea, with all four rounds in it from the start.

Play the result: [oneshot.inkon.co.uk/pkt-8](https://oneshot.inkon.co.uk/pkt-8/) · More at [www.inkon.co.uk](https://www.inkon.co.uk)

---

## The prompt

Build **PKT-8**, a pocket drum machine and acid bass line groovebox for making house and dance loops. It runs entirely in the browser as one self-contained HTML file (no server, no keys, no install), and all sound is synthesised live with Web Audio, with no samples. It is inspired by compact TR-style rhythm machines with a 303-style bass, but never names them. It opens with seven demo grooves loaded, so pressing Start immediately plays something good. Meet every acceptance criterion below, then self-check each one and run the polish pass before you call it done.

## Reference and core loop
- **Inspired by:** a compact TR-style rhythm machine with a 303-style bass line.
- **Signature interactions:**
  - 16 step keys in red/orange/yellow/white groups of four,
  - per-instrument sound tweaks,
  - accent, sub-steps (ratchets) and probability,
  - bass notes with accent and slide,
  - "scatter" performance effects and sidechain pumping.
- **First 10 seconds:** press Start and hear a groove, then tap a style and hear a whole new track.
- **Minute 50:** performing a track live with sections, fills, risers and drops, and recording clips.
- **Audience:** bedroom producers and the curious · music-making TikTok.

## Assumptions
- Browser-only, so every sound is synthesised (Web Audio). No sample files.
- A 16-step grid with a pattern length of 1–16, and 8 pattern slots A–H.
- House subgenres for the styles.

## Acceptance criteria

### Core
- [ ] Drums:
  - BD, SD, Rim/Perc, Clap, Closed Hat and Open Hat (the closed hat chokes the open hat).
  - Each has level, tune, decay and an FX send.
- [ ] An accent row with an amount control.
- [ ] A chords row that follows the key and scale and shows chord names.
- [ ] A bass line row with a note keyboard, octave, and accent and slide per step.
- [ ] Step edit modes: Trig / Probability (100/75/50/25%) / Sub-step (1–4).
- [ ] A lookahead Web Audio scheduler, swing, tempo 60–200 with tap tempo.
- [ ] FX and mixing:
  - tempo-synced delay (1/8, 3/16, 1/4),
  - reverb and drive,
  - sidechain from the kick,
  - a DJ filter (low-pass ↔ high-pass),
  - a master compressor.
- [ ] 8 pattern slots. Switching waits for the end of the bar; also copy/paste and pattern length.

### Variety and generation
- [ ] **Styles:** Deep, Chicago, Tech, Acid, Progressive, Afro and Minimal House.
  - One press writes all 8 sections: Intro, Groove, Main, Main 2, Break, Build, Drop, Outro.
  - Each style picks the kit, bass and chord sounds, scale, chord progression, tempo, swing and FX.
- [ ] **Sound swap (↻) on every row:**
  - Kick: 909, 808, Deep, Punch
  - Snare: 909, 808, Tight
  - Perc: Rim, Cowbell, Conga, Shaker
  - Clap: 909, 808, Snap
  - Hats: 909, 808, 606
  - Chords: Organ, Deep Chord, Arp, Pad
  - Bass: Acid Saw, Acid Square, Sub, Reese, Organ
- [ ] **Generation controls:**
  - New part (the selected row, in the current style),
  - Mutate,
  - Evolve (small changes every 2 bars),
  - a key and scale selector that transposes everything.
- [ ] Song mode plays A→H at 1, 2, 4 or 8 bars per section.

### Safety nets
- [ ] Reset with a two-tap confirm.
- [ ] Undo (30 steps, covering whole-track generation).
- [ ] Auto-save in the browser, with version migration.

### Platform
- [ ] Single HTML file. On a phone, the grid scrolls inside its own panel.
- [ ] Space starts and stops; keys 1–6 are performance pads.
- [ ] A dark hardware look: one display face, one UI face and one mono face for the LCD, with the TR step colours.

### Name and brand
- [ ] Name: PKT·8. No third-party names or logos. Optional credit line on the faceplate.

### Share mode
- [ ] A 9:16 canvas screen showing the name, style, section, tempo, key, an oscilloscope, the step grid and a section strip.
- [ ] Nine big pads: Start/Stop, New Track, Next Style, Fill (hold), Cut Low (hold), Stutter (hold), Next Section, Swap Sound, and Riser (hold to sweep the filter, let go to drop).
- [ ] An optional built-in recorder: MP4 with audio, plus 15, 30 and 60 second auto-stop.

## Finish line
Before saying it's done:
1. Check every acceptance criterion above and fix anything missing.
2. Screenshot desktop, phone and share mode. Critique like an Apple designer with at least 12 ranked flaws, and fix every high and medium one.
3. Run one more short round: "what still looks unfinished?"
