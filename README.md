# Möbius Bar Player

The official player of the Möbius Bar, the main bar of the world.
Music, lava-lamp and disco lights, and moods that change slowly, all on one fixed square stage that looks the same on a phone and a computer.

**Open it:** https://ovidemetrian.github.io/MOBIUS-BAR-PLAY-THE-LAMP/

**Mini Player:** https://ovidemetrian.github.io/MOBIUS-BAR-PLAY-THE-LAMP/mini/ (your own songs from the phone, the live wave, and a one-tap video for YouTube). If the big player is already on your home screen, press and hold its icon and pick **Mini Player**.

## What it does

- **Three pages:** Bar (now playing, meter, lights) · Tracks (play, keep, let go) · Set (your kept set). Swipe, use the arrows, or press ← →.
- **Six moods:** Aurora, Lava, Disco, Rainbow, Neon, Candle. Switching moods blends the colours over a few seconds. **Auto mood** moves to the next mood every 40 seconds.
- **Beat sync:** the lights read the music (Web Audio), so the blobs swell, the beams open and Disco/Neon flash on the kick. Turn it off and the lights breathe on their own.
- **Meters:** Wave (sine), Bars (jumping lines with peak caps), Ring, or Off.
- **Show mode:** after 30 seconds without a touch (or tap **Show**), the controls fade and the whole screen becomes the light show. Ovi's neon Möbius Bar sign floats over everything (five signs take turns at random). Drag it with a finger or fling it. **Tap it once for a surprise** (mood swing, confetti, fireworks, colour storm, mirror ball, spin, clones, zoom, shockwave, bubbles, lights-out bang, new paint, bubble rain, and now and then a jackpot). Double-tap to play or pause. **Hold it** and everything disappears: the whole screen becomes the pure lamp, colours moving with the music, changing moods and styles on its own. In the lamp, tap anywhere to bring the square back. With the square showing, tap outside it to come back to the bar.
- **Catch the bubbles:** soap bubbles drift in. Fling the sign into them to pop them; the golden ones set off a surprise. It all runs offline, so it works in airplane mode. The screen stays awake while the show is on. To use real cover art, add `art: "art/cover.jpg"` to a track.
- **Kept set** is remembered on the device. **Play kept set** plays the kept tracks in order and loops.
- **About page:** tap the **MADE BY OVI** badge for what the app is, how to use it and how it was made (drag the badge to move it). The text lives in the `about` block in `index.html`; `about.js` draws the page.
- **Installable PWA:** add it to the home screen. The app works offline, but the music still streams.

## Add the music

The first three holders are deep red, dark gold and blue. Green, purple and lilac are open slots: tap **Choose**, pick any song, and the slot takes its name for that visit.

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
