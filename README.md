# SlouchPotato

**MEND your posture instead of ENDING your posture.**

SlouchPotato is a lightweight Windows desktop app that watches your posture through your webcam and grows an increasingly large potato on your screen whenever you start slouching — shrinking away the moment you sit up straight again. No subscriptions, no accounts, just a persistent nudge to keep your back healthy while you work.

---

## Download

Download the latest installer: [**[SlouchPotato-Setup-1.0.1.exe](SlouchPotato-Setup-1.0.1.exe)**](https://github.com/HuuNguyen35/Slouch-Potato-Releases/releases/download/v1.0.2/SlouchPotato-Setup-1.0.2.exe)

Run the installer and follow the wizard. No extra software required — everything is bundled.

---

## How it works

SlouchPotato uses your webcam and Google's **MediaPipe** pose detection to track the position of your nose in real time. When you calibrate, it records your nose's vertical position as your "good posture" baseline. If your nose drops more than a threshold below that baseline (i.e. you've started hunching forward), a potato image appears on your screen and steadily grows the longer you stay slouched. As soon as you straighten up, the potato vanishes.

The detection runs entirely on your machine — no video is sent anywhere.

---

## Features

- **Webcam-based posture detection** — uses pose landmarks, not just face detection, for accuracy
- **Growing potato overlay** — a playful but impossible-to-ignore visual reminder that floats above all windows without stealing focus or blocking clicks
- **One-time calibration** — press Space in the dashboard to lock in your upright posture as the reference point
- **System tray integration** — reopens the dashboard if you close the window; a second launch brings it back instead of starting a duplicate
- **Optional startup with Windows** — set during installation so SlouchPotato is always on guard
- **Optional desktop shortcut** — choose during installation whether to add one

---

## Installation

1. Download **SlouchPotato-Setup-1.0.1.exe** from this folder.
2. Run the installer (administrator rights required).
3. Optionally tick:
   - **Create a desktop shortcut**
   - **Launch SlouchPotato when Windows starts**
4. Click **Finish** — SlouchPotato launches immediately.

---

## First-time setup

1. SlouchPotato opens and your webcam feed appears in the dashboard.
2. **Sit up straight** in your normal working position.
3. Press **Space** (or click inside the dashboard and press Space) to calibrate.
4. The overlay bar turns green — you're good to go.

From now on, whenever your nose drops below your calibrated position the potato will appear. Sit up and it disappears.

---

## System requirements

| | |
|---|---|
| OS | Windows 10 / 11 (64-bit) |
| Webcam | Any USB or built-in webcam |
| RAM | ~200 MB |
| Disk | ~150 MB |
| Permissions | Administrator (for installation only) |

---

## FAQ

**Does SlouchPotato send my video anywhere?**
No. All processing happens locally on your machine using MediaPipe. Nothing leaves your computer.

**The camera feed shows "Please turn on your camera!" — what do I do?**
Check that no other application (Teams, Zoom, OBS, etc.) has exclusive access to your webcam. Close those apps or switch their camera off, and SlouchPotato will reconnect automatically.

**The potato appeared when I wasn't slouching.**
Re-calibrate: open the dashboard, sit up straight, and press Space again.

**How do I uninstall?**
Go to **Settings → Apps** (Windows 11) or **Control Panel → Programs and Features** (Windows 10) and uninstall SlouchPotato from there.

---

## Source code

The source code is available at the parent repository. Built with Python, PyQt6, OpenCV, and MediaPipe. Packaged with PyInstaller and Inno Setup.
