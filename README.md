# 🎙️ VOICE_LINK v1.5 (P2P Radio)

![Version](https://img.shields.io/badge/version-1.5-neon.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![Tech](https://img.shields.io/badge/WebRTC-PeerJS-blue)

A high-performance, low-latency **Peer-to-Peer Voice Communicator**. 
Designed with a "Walkie-Talkie" interface, this web app establishes a direct audio link between two users using specific frequencies (Channels).

## ⚡ Key Features

* **🔒 Private & Direct:** Audio streams travel directly between devices (Peer-to-Peer) via WebRTC. No audio data is stored on any server.
* **🤝 Robust Handshake Protocol:** Version 1.5 introduces a new `ACK` based name exchange system. It ensures user Codenames are synced 100% of the time, even on slow connections.
* **📻 Frequency Based:** No complicated URLs. Just agree on a 4-digit "Frequency" (e.g., `1111`) to pair devices.
* **🌑 Cyberpunk UI:** Minimalist, high-contrast Dark Mode interface designed for OLED screens and low-light operations.
* **👆 Push-to-Toggle:** Large, tactile microphone control. Click to go **"ON AIR"**.

## 🚀 Live Demo

[**Click here to Launch App**](https://wifitalk.netlify.app/)
## 🛠️ How to Use

### 1. Establish a Command Post (Host)
1.  Open the app.
2.  Enter your **Codename** (e.g., `ALPHA`).
3.  Enter a **4-Digit Frequency** (e.g., `5050`).
4.  Click **CREATE**.
5.  Wait for the status to say "Waiting for Partner...".

### 2. Join the Frequency (Guest)
1.  Open the app on a second device.
2.  Enter your **Codename** (e.g., `BRAVO`).
3.  Enter the **Same Frequency** (`5050`).
4.  Click **JOIN**.

### 3. Communication
* Once connected, the screen will display **"LINKED: [PARTNER NAME]"**.
* Click the big **MIC OFF** button. It will turn **Green (ON AIR)**.
* Speak. Click again to mute.

## 📦 Installation / Deployment

**Important:** Because this app uses the Microphone, modern browsers require it to run in a **Secure Context (HTTPS)**.

### Option A: GitHub Pages (Recommended)
1.  Upload `index.html` to a GitHub repository.
2.  Go to **Settings** -> **Pages**.
3.  Deploy from `main` branch.
4.  Your radio is now live and secure.

### Option B: Local Testing
You **cannot** run this by double-clicking the file (`file://`).
You must run a local server:

```bash
# Python
python3 -m http.server 8000

# Node.js
npx http-server

