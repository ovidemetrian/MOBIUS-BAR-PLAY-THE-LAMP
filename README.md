# Möbius Bar Player

The official player of the Möbius Bar, the main bar of the world.
Music, lava-lamp and disco lights, and moods that change slowly, all on one fixed square stage that looks the same on a phone and a computer.

**Open it:** https://ovidemetrian.github.io/MOBIUS-BAR-PLAY-THE-LAMP/

## What it does

- **Three pages:** Bar (now playing, meter, lights) · Tracks (play, keep, let go) · Set (your kept set). Swipe, use the arrows, or press ← →.
- **Six moods:** Aurora, Lava, Disco, Rainbow, Neon, Candle. Switching moods blends the colours over a few seconds. **Auto mood** moves to the next mood every 40 seconds.
- **Beat sync:** the lights read the music (Web Audio), so the blobs swell, the beams open and Disco/Neon flash on the kick. Turn it off and the lights breathe on their own.
- **Meters:** Wave (sine), Bars (jumping lines with peak caps), Ring, or Off.
- **Show mode:** after 30 seconds without a touch (or tap **Show**), the controls fade and the whole screen becomes the light show. The song's artwork floats around as a square. Drag it with a finger or fling it. **Tap it once for a surprise** (mood swing, confetti, fireworks, colour storm, mirror ball, spin, clones, zoom, shockwave, bubbles, lights-out bang, new paint, orb rain, and now and then a jackpot). Double-tap to play or pause. Tap anywhere else to come back.
- **Catch the orbs:** glowing orbs float in. Fling the artwork into them for points, chain catches for up to ×5 combos, and golden orbs are worth 5 and set off a surprise. Your best score is saved. It all runs offline, so it works in airplane mode. The screen stays awake while the show is on. To use real cover art, add `art: "art/cover.jpg"` to a track.
- **Kept set** is remembered on the device. **Play kept set** plays the kept tracks in order and loops.
- **Installable PWA:** add it to the home screen. The app works offline, but the music still streams.

## Add the music

The first three holders are deep red, dark gold and blue. Green, purple and maroon are open slots: tap **Choose**, pick any song, and the slot takes its name for that visit.

Put the files in `audio/` with these names:

```
audio/nose-on-the-glass.mp3
audio/future-past.mp3
audio/the-studio-in-my-hand.mp3
```

To add or rename tracks, edit the `tracks` list near the top of the script in `index.html`. Each track has an `id`, `title`, `color`, `src` and an optional `note`.
If a file is missing, the card shows **Choose**, which plays a file from the device for that visit.

Audio from another website only drives the lights if that server allows CORS. Files kept in `audio/` always work.

## Publish on GitHub Pages

Settings → Pages → Deploy from a branch → `main` / root → Save.

After changing files, raise `CACHE` in `sw.js` (for example `v6` → `v7`) so installed copies update.

---

Concept & design: **Ovi Demetrian** · built with Claude
