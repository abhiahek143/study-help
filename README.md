# Together - Watch & Talk

Together is a simple browser app for watching YouTube videos with a friend while staying on a live video call. Both users join the same room code, load a YouTube link, and playback actions like play, pause, seek, and video loading are synced through a PeerJS data connection.

## Features

- Join a shared room with a short room code
- Start a direct browser-to-browser video call
- Load YouTube links or 11-character YouTube video IDs
- Sync YouTube playback between two people
- Keep a call timer while the remote video stream is active
- No app ads, backend, database, account system, or saved user data

## Tech Stack

- HTML, CSS, and vanilla JavaScript
- PeerJS for WebRTC peer connections
- YouTube IFrame Player API for embedded playback
- Public STUN/TURN servers for better call connectivity

## Project Files

```text
.
├── index.html   # Complete app: layout, styles, and JavaScript
└── README.md    # Project documentation
```

## How To Run

This project is static, so it does not need npm or a build step.

1. Start a local static server:

   ```bash
   python3 -m http.server 8000
   ```

2. Open the app in your browser:

   ```text
   http://localhost:8000
   ```

3. Allow camera and microphone access when the browser asks.

## How To Use

1. Open the app in a modern browser.
2. Type a room code, for example `movienight`.
3. Ask your friend to open the same app and enter the same room code.
4. Paste a YouTube URL or video ID into the input box.
5. Click **Load**.
6. Play, pause, or seek the video. The same action will be sent to the connected friend.
7. Use **Unmute friend** if the remote video tile is muted by the browser.
8. Click **Leave room** to disconnect.

## Browser Notes

- Camera and microphone access require a secure browser context, such as `localhost` or an HTTPS deployment.
- Both users need internet access for PeerJS, the YouTube player, and YouTube video playback.
- The app itself does not include ads. YouTube may still show its own ads inside the embedded player.
- If a video call does not connect on a strict network, try another browser, network, or HTTPS deployment.

## Deployment

Because the app is only one HTML file, it can be deployed on any static hosting service, such as GitHub Pages, Netlify, Vercel, or Cloudflare Pages.

## Privacy

Together does not store messages, video, room codes, or watch history. The app runs in the browser and uses peer-to-peer browser connections for the room and call.
