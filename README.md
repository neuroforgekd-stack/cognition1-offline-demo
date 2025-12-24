# Cognition One — Offline Demos (v1, v2, sandbox)

## What it is

Single-file HTML demos for video prototyping. These are client-side only: no backend, no uploads, and no recording by default.

## Files

- `cognition_one_offline_video_demo.html` — v1 demo
- `cognition_one_offline_video_demo_v2.html` — v2 (minimalist UI, theme, and Script Mode)
- `cognition_one_offline_video_demo_analysis_sandbox.html` — sandbox for analysis/testing

## How to run

- Easiest: double-click any HTML file to open in your browser.
- For full sensor support (getUserMedia) serve locally:

```bash
python -m http.server 8080
# then open http://localhost:8080/cognition_one_offline_video_demo_v2.html
```

## Script Mode hotkeys (v2)

- `K` — Toggle Script Mode ON/OFF (shows small "SCRIPT MODE" badge)
- `1` — All clear (force riskSmooth = 0.12)
- `2` — Pay attention (force riskSmooth = 0.38)
- `3` — Slow down (force riskSmooth = 0.62)
- `4` — Verify first (force riskSmooth = 0.86)
- `0` — Release control (return to live computed riskSmooth)
- `C` — Toggle Cue overlay (visual only)
- `Q` / `W` / `E` / `R` — Set cue label to Scene 1..4 respectively

## Browser permissions / notes

- When opened via `file://` some sensor APIs are restricted by the browser. Serve from `http://localhost` for full sensor functionality.
- The demos are designed for offline video prototyping and do not upload audio/video to any server.
