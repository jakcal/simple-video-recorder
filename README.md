# Recorder

A single-file, browser-based video recorder. Capture from your camera and microphone, review the clip, keep it in a local library, and download it. Nothing is uploaded — every recording stays in your browser's storage on your own device.

**Live demo:** [jakcal.github.io/simple-video-recorder](https://jakcal.github.io/simple-video-recorder)

## Features

- **Camera + microphone capture** with a live viewfinder, tally strip, and a REC lamp
- **Device and quality pickers** — switch camera, microphone, and resolution (480p → 4K) without reloading
- **Pause and resume** mid-recording, with a timer that excludes paused time
- **Keyboard transport** — <kbd>Space</kbd> to start/stop, <kbd>P</kbd> to pause
- **Live microphone meter** driven by a real `AnalyserNode`, so you can see you are actually being picked up
- **Automatic codec selection** — VP9/VP8 WebM where available, H.264 MP4 on Safari
- **Local library** in IndexedDB: play, download, and delete past recordings
- **Storage read-out** showing how much of the browser's quota is in use
- **Honest failure states** for blocked permissions, a busy camera, a missing device, or an insecure page

## Requirements

Recording needs a **secure context**: `https://` or `http://localhost`. Opening `index.html` straight from the filesystem (`file://`) leaves `navigator.mediaDevices` and `navigator.storage` undefined, and the page will tell you so instead of breaking.

To run it locally:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Technologies

- `getUserMedia` for camera and microphone access, `MediaRecorder` for capture
- Web Audio `AnalyserNode` for the input level meter
- IndexedDB for blob storage, `StorageManager.estimate()` for the quota read-out
- Native `<dialog>` for confirmations
- Vanilla HTML, CSS, and JavaScript — no build step, no dependencies

## Browser support

Recent Chrome, Edge, Firefox, and Safari. Safari records H.264 MP4 rather than WebM; the correct extension is applied to downloads automatically. Private/incognito windows may block IndexedDB, in which case recording and downloading still work but the library is disabled.
