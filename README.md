# netRadio

netRadio is a lightweight, browser-based internet radio app for discovering and streaming English-language radio stations. It provides a polished single-page interface with search, category filtering, and AI-assisted station discovery prompts.

## What the application is

The project is a static web application (`index.html`) that:
- Lists curated radio stations with metadata.
- Streams audio directly in the browser via the built-in `<audio>` player.
- Supports category filtering (Music, Talk, Science, Technology, News).
- Includes an AI discovery button for mood-based station suggestions.

A helper script (`deploy.sh`) can package and run the app in Docker with a simple Node static server.

## Basic controls

Inside the app UI:
- **Search input**: Type station names or keywords to narrow results.
- **Category chips**: Filter stations by topic.
- **Station list item**: Click to start playback.
- **Play/Pause controls**: Manage stream playback.
- **Sleep-friendly noise section**: Tap the noise button to cycle `OFF → WHITE NOISE → BLUE NOISE → PINK NOISE → OFF`, then use the mix slider from 0% noise / 100% audio to 100% noise / 0% audio.
- **Sleep timer**: Set a timer (10–60 minutes) to automatically pause playback.
- **✨ Discover button**: Use prompt-style discovery for mood or context-based station ideas.

## Build / run instructions

### Option 1: Open directly
Because this is a static app, you can open `index.html` in your browser.

For older Safari/WebKit devices (for example iPad Mini v1 on iOS 9), use `legacy.html`, which avoids modern dependencies and uses ES5-style JavaScript for better compatibility.

### Option 2: Run with Docker deploy script
```bash
./deploy.sh 3000
```
Then visit `http://localhost:3000` (or the local IP printed by the script).
The deployed container serves both `index.html` and `legacy.html` (open `/legacy.html` for older iPad/Safari clients).

## Roadmap

Short-term ideas for future improvements:
- Add persistent favorites and recently played stations.
- Add dark/light theme switching and accessibility refinements.
- Add health checks with automatic stream fallback on failure.
- Add keyboard shortcuts for search, play/pause, and volume.
- Add optional backend endpoint for richer AI station recommendations.
