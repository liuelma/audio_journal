# Journal Recorder (MVP)

Free MVP: iPhone-friendly web app (PWA) that:

- Records audio (optional storage to save space)
- Uses the phone/browser's built-in Speech-to-Text (STT) when available
- Generates a local bullet summary
- Stores transcript + summary on-device for later search

## Files

- `index.html` (all UI + logic)
- `manifest.webmanifest` (for “Add to Home Screen”)

## Run it on your iPhone (free)

1. Upload `index.html` and `manifest.webmanifest` to a new GitHub repository.
2. Enable GitHub Pages for that repo (Settings -> Pages).
3. Open the GitHub Pages URL on your iPhone using Safari.
4. Tap Share -> Add to Home Screen.

Note: Speech recognition and recording features require permissions and may behave differently depending on iOS/Safari versions.

## Transcription behavior (important)

This MVP uses the Web Speech API (`SpeechRecognition` / `webkitSpeechRecognition`) in the browser.
If speech recognition is unavailable in your browser, the app will still let you type/paste a transcript and then generate bullets + search normally.

## Language

The app has a language selector (`English` or `Mandarin Chinese`) which is used for:

- Setting the speech recognition language (`en-US` vs `zh-CN`)
- Local keyword and bullet extraction heuristics

## Storage minimization

- Default: audio is NOT stored. Only transcript + bullet summary are saved.
- If you enable “Keep audio on-device”, the app will also store the recorded audio blob (uses more storage).

