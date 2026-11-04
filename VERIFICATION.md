## Framevik verification (Oct 27 – Nov 3, 2026)

- Build history: the Framevik project's versions v1–v39 are
  recorded inside the CODREN project (build chat, project files,
  version history). No aggregate call total is claimed here.
- v25: AI Editor brief-from-zero, handoff and scope-refusal pass;
  a garbled duplicate title can appear beside the correct one
  (defect, disclosed).
- v26: Reference Match applies real, editable Lumetri values.
- v27: the look-strength setting was ignored by the build (defect,
  disclosed). Meta-use evidence is the CODREN call log.
- v28: keyboard shortcuts pass; clip-edge drag-trim unreliable
  (defect, disclosed).
- v29: fake waveform removed; honest "No audio" lanes; scopes
  proven driven by the real frame.
- Direct build (Oct 29): the interface was rebuilt directly in code
  as a one-viewport grid and packaged as the installable Framevik
  Studio desktop app; interface parts found unstyled in code (panel
  tabs, audio meters, timeline head; scopes/audio strip inside the
  Program monitor) were fixed the same day.
- v15: the Program image fills the monitor scene (measured at the
  owner's laptop size). The owner's verdict on the screens:
  accepted — the interior functions were still open at that point.
- v16: clip dragging along/across tracks (tested 0.0 s → 4.0 s);
  dark fields replace the white ones; "Drop clips here" text
  removed; multi-select, Cmd+A and Delete; right-click clip menu
  tested working.
- v17: project persistence fixed (the app previously saved nothing
  and mixed up project IDs, so the demo project reopened every
  time); real-frame thumbnails; real playback; a new project
  starts truly empty with the chosen name. Re-import-on-reopen
  limit noted in the README.
- v18: Program sound; real audio waveform read from the file;
  Speed 25–400% (tested: 200% plays at playbackRate 2); In/Out
  marking with range-only export; drag-and-drop effects onto a
  clip (tested: applied count became 1 after drop); real-frame
  export. Export audio still absent at this version, disclosed.
- v19: per-clip source in-points; splits, left trims, playback and
  export all respect the cut, and cuts survive close/reopen
  (verified numerically: split at 2.8 s starts media at 2.8 s;
  ~1.2 s left trim shifts media by exactly the trim). These are
  measurements on the direct build — the owner's overall verdict
  on the CODREN-line builds of this period was negative (a later
  version was rejected outright on Oct 31, and the direct build
  was judged to still feel like a prototype); the numbers stand
  as measurements, not as his endorsement.
- v20 (Oct 30): export audio FIXED in the direct desktop build —
  the render pass carries the audio track; a 440 Hz tone clip
  exported and measured at RMS 0.274 against a 0.282 source.
- v21 (Oct 30): effects measured in the exported file — Gaussian
  Blur −35% edge sharpness, Sharpen +27%, Halation +4.7% export
  light, Bass +25% energy; titles render into the export exactly
  as designed (color/position verified). Stabilize, Remove
  Background and Balance were REMOVED from the effects list
  entirely because they were not real; Denoise and Face Retouch
  are not claimed.
- Oct 31 — the CODREN rebuild, method rounds: the editor's core was
  rebuilt in CODREN under a stricter method: the project model
  carries a per-clip source in-point, every edit is one undoable
  command, and one renderer serves the Program monitor and the
  export.
  - Round 1 (model): PASSED the reviewer's code audit on v35 —
    split keeps the source point (right half starts at source 3.8
    after a split at 2.8), trim advances the source point, speed
    preserves the source span, ripple move shifts followers by the
    same delta, and playback/export resolve source time through
    the same helper.
  - Round 2 (shared renderer + export audio): first attempt (v36)
    changed only the shell file and reported no measurements —
    rejected as unproven. A strict directive followed: remove all
    reference-product branding, ship the approved Framevik logo,
    and add the in-app Self-test screen (final state below).
- Nov 1 — branding micro-step (saved v38): exactly the app-name
  strings changed; header/footer/title read "Framevik Studio",
  project files carry the ".framevik" name. Audited in exported
  source: zero user-facing reference-product strings remain.
- Nov 1 — FRAMEVIK-LAW.md added to the CODREN project root (v39),
  verbatim as ordered; the only file changed in that version.
- Nov 1 — Self-test screen: the CODREN build of this step failed
  twice on the platform side (the second attempt returned
  "The build can't start right now"). The Self-test screen was
  therefore completed by Muse directly on the exported v39
  source: real store, real component, executed under jsdom, the
  result table read from the DOM — 7/7 checks PASS with measured
  values: split at 2.8 → srcIn 3.8, duration 5.2; trim start to
  4.0 → srcIn 5.0, duration 4.0; speed 2× → source span 4.0,
  timeline duration 2.0; split after speed → srcIn 7.0; ripple
  A → 2 → B starts at 6.0; volume 1.5 → stored value clamps to 1;
  the same effect applied twice → 1 entry, latest amount.
- Nov 2 — export proof on the final build: a clean edit was built
  in the app (concert footage cut at 20 s and 35 s into three
  pieces plus a stage clip, the song on the audio track, Sharpen
  on the second piece, contrast +50 on the first, English title
  "Concert Highlights") and the exported file was verified outside
  the app: 69.9 s, the song's audio throughout (RMS −12.1 dB
  against the source's −12.3 dB), the title composed inside the
  file. Self-test still 7/7 on the same build.
- Nov 3 — export crossfade: measured on the exported file as a
  true two-picture blend (outgoing weight 1.00 → 0.83 → 0.48 at
  the midpoint → 0.11 → 0). The in-app Monitor preview does not
  blend (single video element) — disclosed; the blend is claimed
  for the export only.
- Final verified build: Framevik project version 39 — the
  Self-test measurements (Nov 1) and the export proof (Nov 2)
  were taken on this source.
- Demo video: https://youtu.be/V-F-R3J2LcE — 3 minutes, showing only work built
  during the event, and only functions on the verified list
  above.

## Push-day checklist (unchanged duties, from V3/V4/V5)

1. Re-read the Framevik call log → fill the build-calls line.
2. Fill the final-version line from the last verified build.
3. Add the demo video URL after the final render.
4. Push README + VERIFICATION only — no source, no keys, no
   routing/cost internals.
5. Open the repo logged-out and confirm it loads (submission rule).
