---
name: oneshot
description: Turns a rough one-line idea into a complete, paste-ready "one shot" build prompt for Claude Code. The prompt already contains everything you'd normally only ask for in follow-up rounds (presets and a generator, undo and reset, saving, mobile, original naming, a polish pass), so the first build is the finished build. Use when the user types /oneshot, or asks for a one-shot prompt, a build prompt or a spec for an idea.
---

# /oneshot: get an amazing one-shot prompt

Most builds take four or five prompts. The first gets something working. Then come the predictable follow-ups: "add a reset", "give me presets", "it needs to work on my phone", "make it feel finished". This skill writes those into the **first** prompt, so one shot is enough.

**Input:** everything after `/oneshot` is the idea, e.g. `/oneshot a pocket drum machine I can make dance music on`. A photo or link of the thing that inspired it helps.

**Output:** one self-contained prompt, saved as a Markdown file, ready to paste into a fresh Claude Code session (or build straight away if the user says "build it").

## Step 1: Pin the idea

Work out these four things from the one line, plus any photo or link:
- **Reference:** the real thing it's inspired by, and the *workflow* people love about it (how it's used, not just how it looks). Name 3–5 signature interactions.
- **Core loop:** what someone does in the first 10 seconds, and what keeps them going at minute 50.
- **Audience:** who will use it, and who will see it shared.
- **Original name:** a product name that isn't a trademark (e.g. "PKT-8"). Never use the real product's brand or model name in the prompt's output.

## Step 2: Ask only what matters

Ask **at most 3** questions, all in one go, and only where a wrong guess would mean a rebuild (e.g. "a synth" could be a keyboard instrument or a modular patcher). Everything else gets a sensible default, written under **Assumptions** in the prompt. If nothing is genuinely ambiguous, ask nothing.

## Step 3: Write the prompt

Fill in `prompt-template.md`. Go through every item in `checklist.md` and turn each one into a concrete line **for this idea**:
- "Style buttons: Deep, Tech, Acid, Piano…", not "has presets".
- "Reset with a two-tap confirm", not "safety features".

If an item doesn't apply, drop it or say why in one line.

**Rules for a great one-shot prompt:**
- **Self-contained.** It must work pasted into a brand-new session with no history.
- **Specific.** Real names, real numbers, real lists. Vague prompts get generic builds.
- **Complete, not a starter.** Ask for the whole thing, with demo content loaded so the first screen already shows what it does.
- **Browser-first by default.** A single HTML file with no server, keys or installs, unless the user says otherwise.
- **Ends with a finish line.** The prompt must tell the builder to self-check every acceptance criterion and run the polish pass before calling it done.

## Step 4: Check it, save it, hand it over

1. Re-read the prompt against `checklist.md`. Fix any gaps.
2. Save it as `oneshot-prompts/NNN-<slug>.md` in the current project, where NNN is the next free 3-digit number.
3. Show it to the user in full, then offer two options: paste it into a fresh session, or say **"build it"** to build it now.

## Step 5: Learn from misses

If the user still asks for a change after the build, that's something the prompt should have included. Add a short, **general** line to the "Lessons" section at the bottom of `checklist.md` (e.g. "creative tools need undo for destructive actions", not "PKT-8 needed undo"). That way every future prompt includes it.
