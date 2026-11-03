# Recap

Merge your logs into one timeline.

Drop in CSV, TSV or JSON exports from different tools and Recap finds the timestamps, merges everything in UTC, and charts it. Zoom into bursts, filter, tag the key events with ATT&CK-style phases, and export the story.

**Good for:** Event logs, Sysmon, proxy, $MFT and EDR exports from the same incident, side by side.

**Live:** https://jon.glass/recap/

A single self-contained page with no build step. Open `index.html` or serve the folder over HTTPS.

Uses the shared suite script at `/assets/suite/handoff.js` from [jon.glass](https://jon.glass) to pass data between tools, so cross-tool handoff only works when served from jon.glass.
