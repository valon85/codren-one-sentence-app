# CODREN — One-Sentence App, Live

This is CODREN (codren.ai), an AI creation platform powered by
Meta AI.
CODREN turns one sentence into real software. You describe what you
want, and CODREN plans the work, then generates the interface, the
logic, the database, and the connections, and shows you the result
live, ready to use.

You can talk to it like a chat, or put it to work like a builder.
New models are absorbed once, inside CODREN, while the products
built on it keep working. One engine, maintained in one place,
powering everything we ship.

For this competition, CODREN runs on Meta AI — and what we built
with it, from zero, during this event, is Framevik (framevik.com).

## Framevik — a professional video editor built during the event

Framevik (framevik.com) is a professional desktop video editor, in
the class of Adobe Premiere and DaVinci Resolve, built with CODREN
and Meta AI during the event window (Oct 26 – Nov 4, 2026) and
packaged as an installable desktop app — Framevik Studio
(Electron) — for Mac and Windows.

Framevik was created inside this competition — and it does not end
with the competition. It continues as a real product, and a real
business, built to be used by working editors.

Verified during the build:

- One-viewport editor surface at desktop size: media bin, dual
  monitors (Source and Program), grouped inspector, and an
  always-visible timeline whose playhead line spans ruler and lanes.
- Real editing on your own footage: import a video and it appears
  with its real frames as thumbnails in the bin, on the timeline
  and in the monitors. The Program monitor plays the real video,
  with sound, synced to the playhead and at the clip's real
  duration. The clip shows the audio waveform read from the file
  itself — and clips with no audio honestly say "No audio"; the
  editor does not draw fake waveforms.
- Projects persist: close the app and reopen it and the project,
  clips and cuts are still there. A new project starts truly empty
  under the name you give it. (Limit, stated openly: after a
  reopen, an imported video keeps its thumbnail and timeline place
  but must be re-imported once to play again — the app does not
  copy media files into itself.)
- Timeline editing the way editors work: clips can be dragged along
  and across tracks, selected (click, Shift+click, Cmd+A), deleted,
  and managed from a right-click menu (Split at Playhead, move,
  transitions, Select All, Delete). Every clip keeps its source
  in-point, so a cut stays cut: split a clip and the second part
  plays from the cut point — in playback, after a left trim, in
  export, and after reopening the project (verified numerically:
  split at 2.8 s; a ~1.2 s left trim shifts the source point by
  exactly the trim). Ripple moves shift following clips by the
  same delta.
- Speed 25–400% per clip. In/Out marking on the ruler, with Export
  rendering only the marked range.
- Keyboard editing: Space (play/pause), C (cut), J/K/L (shuttle),
  V (selection) all verified.
- Color: 12 cinematic looks and Lumetri-style controls; four scopes
  (Waveform, RGB Parade, Vectorscope, Histogram) proven driven by
  the real frame.
- Effects proven to render: Chroma Key (green/blue — the green is
  removed and the foreground stays intact on the built-in test
  asset) and Gaussian Blur. Effects were also measured inside the
  exported file on the installed app: Gaussian Blur −35% edge
  sharpness, Sharpen +27%, Halation +4.7% export light, Bass +25%
  energy. Effects are applied by dragging them from the Effects
  panel onto a clip.
- Titles are fully styled — text, color, and position — and render
  into the export exactly as designed (color and position verified
  in the exported file).
- Crossfade transitions: in the exported file the crossfade renders
  as a true two-picture blend (pixel-measured, Nov 3: outgoing
  picture weight 1.00 → 0.83 → 0.48 at the midpoint → 0.11 → 0).
  The Program monitor preview does not yet show the blend — stated
  openly; the blend is claimed for the export only.
- Export produces a real file, picture and sound together. Exported
  files carry the audio track, verified by measurement on the
  installed app (a 440 Hz tone clip exported and measured at RMS
  0.274 against a 0.282 source). On Nov 2 a clean edit (concert
  footage cut in three places plus a stage clip, a song on the
  audio track, Sharpen and contrast applied, an English title) was
  exported and verified on the exported file itself: 69.9 s, the
  song's audio throughout (RMS −12.1 dB against the source's
  −12.3 dB), the title composed inside the file.
- AI Editor: a scoped editing worker — it takes a brief from zero,
  continues from a human's halfway edit ("handoff"), applies the
  steps to the current project, and refuses non-editing questions.
- Reference Match: attaching a reference photo/video applies real,
  editable Lumetri values matched from it.
- AI captions/translation: timed captions typed in the app can be
  translated by the AI layer (verified Albanian → English). Where
  no licensed voice exists for a language, the app says so instead
  of faking a spoken dub. There is no AI dub voice.
- Self-test: the app carries an in-app verification screen that
  runs the acceptance checks against the live project store and
  prints measured values — 7/7 checks pass (values in
  VERIFICATION.md). Who built that screen is stated in the
  authorship note below; it was not built by CODREN.

### Authorship note (exact honesty, from the V5 delta)

Framevik was built with CODREN and Meta AI (Muse Spark) during the
event window. The in-app Self-test verification screen was added by
Muse (Meta AI) directly on the final event source after the CODREN
builder hit a platform limit; its 7/7 measured results verify the
CODREN-built timeline model (the per-clip source-in-point
architecture from the Oct 31 Round 1 audit). CODREN did not build
the Self-test screen, and the Self-test values never came from
CODREN's own reporting — acceptance was always independent
audit and measurement.

### Honest scope (Framevik)

Export-with-audio is claimed from the installed-app measurements
above (tone test, and the Nov 2 exported-file readback). Effects
and titles in the exported file are claimed from the installed-app
measurements above. The Program monitor preview does not yet blend
crossfades (the export does). Speed/time remapping beyond the
25–400% control, multicam and shows/seasons are post-event work,
by decision — they are not part of this submission.

Demo video: https://youtu.be/V-F-R3J2LcE

## Briovix

Briovix (briovix.com) is a complete social platform with its own
design: feed and stories, trending, messages and talk rooms, a
living map with live places, voice and video calls, live
streaming, and Clips, its short-form video.

Its AI runs on Meta: a chat that answers with Muse Spark, and
image generation created live inside the app (both verified live
on Oct 27, 2026). And when Briovix needs design repairs, the work
goes through CODREN with Meta AI. One engine, behind every
product.

## Spicey

Spicey (spicey.live) is a full social network that stands on its
own, with Meta AI engines integrated directly inside it: AI photo
and video generation, and AI chat, woven into the social
experience. Spicey's Talk Mode runs on OpenAI. In Spicey, the AI
is not a separate destination — it lives where people already
are: in the feed, in the conversation, in the moment a photo is
created and shared.

Spicey was not built with CODREN. But today, when a detail in
Spicey needs changing, the instruction goes to CODREN, and the
change comes back done.

## The pillar

CODREN, with Meta AI, builds the software. Meta AI powers the
experiences. That is what we built for this competition.

---

