# Recap

Merge your logs into one timeline.

Drop in CSV, TSV or JSON exports from different tools and Recap finds the timestamps, merges everything in UTC, and charts it. Zoom into bursts, filter, tag the key events with ATT&CK-style phases, and export the story.

**Good for:** Event logs, Sysmon, proxy, $MFT and EDR exports from the same incident, side by side.

**Live:** https://jon.glass/recap/

### Links that carry their data

`/recap/#input=<base64url>` opens a timeline from data carried in the link itself, the same way Spoke does. The data can be CSV, TSV or JSON, gzipped or not. Optional settings:
- `&name=`: a file name, which also picks the parser by extension
- `&time=`: the timestamp column(s), comma-separated
- `&sum=`: the columns to show as each event's summary
- `&tz=`: an hour offset for times without a zone

Browsers never send the fragment (`#…`) to a server, so the data stays between the page that made the link and Recap. Recap clears it from the address bar once it's loaded.

A single self-contained page with no build step. Open `index.html` or serve the folder over HTTPS.

Uses the shared suite script at `/assets/suite/handoff.js` from [jon.glass](https://jon.glass) to pass data between tools, so cross-tool handoff only works when served from jon.glass.

## License

MIT © 2026 [Jon Glass](https://jon.glass/). Use it however you like; just keep the copyright notice. See [LICENSE](LICENSE).
