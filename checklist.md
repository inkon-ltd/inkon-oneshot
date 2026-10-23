# One-shot checklist

Every one-shot prompt turns each item below into a concrete line for its own idea, or drops it with a one-line reason.

## 1. Faithful core
- [ ] Reproduces the reference's **workflow**, not just its look. Name its 3–5 signature interactions and ask for each one.
- [ ] A real engine, not a mock: audio is actually synthesised, a game is actually playable, a tool produces real output.
- [ ] The right technique for anything timing-critical (e.g. a lookahead audio scheduler, not timers firing sounds).
- [ ] Opens in a **working demo state** (presets or an example loaded), so the first screen shows what it does.

## 2. Variety and generation (usually the third prompt)
- [ ] **Styles, presets or modes:** at least 5, each one press, relevant to what people actually make or play.
- [ ] **One-press generate:** a complete, good result in the chosen style, made from rules per style, not random noise.
- [ ] **Per-element swap:** every major element (sound, colour, piece) has a "next variant" button.
- [ ] **Controlled randomness:** regenerate one part, plus small "mutate" changes.

## 3. Safety nets (usually the second prompt)
- [ ] **Reset to defaults**, with a confirm step built into the page.
- [ ] **Undo** for every destructive action (clear, generate, randomise, reset).
- [ ] **Saves automatically** in the browser (versioned, and tolerant of old saved data).

## 4. Platform
- [ ] Runs **100% in the browser** by default: one self-contained HTML file with no server, API keys, install or login. Cheap to host and works from a link.
- [ ] Works on a **phone**: touch targets at least 44 px, no sideways scrolling, wide content scrolls inside its own panel.
- [ ] Keyboard shortcuts for the main actions, a visible focus ring, and respects reduced motion.
- [ ] Sound (if any) starts from a tap, with a limiter so it never clips.

## 5. Name and brand
- [ ] An original product name. **No third-party trademarks or logos** in the UI, title or file names.
- [ ] Optional: your own credit line on the product (e.g. "One Shot with Inkon").

## 6. Shareable (if it will be posted)
- [ ] A 9:16 **share mode**: a vertical, full-screen view with big controls, ready for screen-recording.

## 7. Polish: the finish line
The prompt must tell the builder to finish with a polish pass:
- [ ] Screenshot desktop, phone and any special mode. Then critique it like an Apple designer, with **at least 12 ranked flaws**, and fix every high and medium one. One more short round for "what still looks unfinished?".
- [ ] Every press responds instantly (a pressed state). Transitions are 120–220 ms with spring easing, and only transform and opacity animate.
- [ ] One spacing scale, one radius scale and one shadow recipe. Aligned baselines. No text under 11 px. WCAG AA contrast.
- [ ] Nothing clipped and no layout shift. A first-run hint shows what to press first. Empty, loading and error states are designed.
- [ ] No console errors. It survives rapid tapping and resizing.

## Lessons
Add a general line here whenever a build still needed a follow-up prompt:
- Creative tools need a reset to defaults with an in-page confirm.
- Tools for making things need one-press styles, a whole-output generator and per-element swaps from the start. People judge a creative tool by how fast it makes something good.
- If it will be shared, build the share mode in from the start.
- A first draft is never the deliverable: always finish with the polish pass.
