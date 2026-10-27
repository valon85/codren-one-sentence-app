# CODREN — One-Sentence App, Live

Meta Global AI Developer Hackathon · Oct 26 – Nov 4, 2026 · Startup track

CODREN is the AI layer behind the live products Briovix (https://briovix.com) and Spicey (https://spicey.live). During this event, that AI layer was switched to run 100% on Meta models — and the switch was verified from the products' own call logs.

## What was done during the event

- **Oct 26 — Meta-only switch, verified.** CODREN's router was switched to Meta-only on the server, with all other engines blocked. A test app built after the switch recorded 9 AI calls — all 9 served by meta/muse-spark-1.3 (see VERIFICATION.md).
- **Oct 26 — One-sentence build flow.** CODREN's prompt → plan → generated-app flow was run end-to-end on Meta models, producing working demo apps.
- **Oct 27 — Briovix AI audited in the live app.** AI Chat answered live (Muse Spark 1.3). Imagine (Muse Image) generated a real image from a text prompt, offered for posting into the feed.

Demo video: to be added before submission.

## What is not in this repo

This repository documents the event work — the flow, the results, and the verification evidence. It does not contain the private source code of CODREN or Briovix, router internals, provider cost logic, API keys, or configuration.

## Links

- https://codren.ai
- https://briovix.com
- https://spicey.live
