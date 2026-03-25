# HeyGopher Desktop

The macOS companion app for [HeyGopher.ai](https://heygopher.ai) — a time-awareness tool that helps you understand how you spend your day on your computer.

## What is HeyGopher?

HeyGopher automatically tracks which applications and websites you use throughout the day and presents that data as a visual timeline. It's not about productivity guilt or micromanagement — it's about giving you an honest, effortless picture of where your time actually goes.

Think of it as a fitness tracker for your work day. You don't have to start timers, tag projects, or remember to log anything. HeyGopher quietly runs in your menu bar, recording what app is in the foreground, and lets you review your day whenever you're curious.

Sync your data to [heygopher.ai](https://heygopher.ai) to see richer analytics, trends over time, and a web-based timeline you can access from anywhere.

## How the Desktop App Works

### Menu Bar App

HeyGopher lives in your macOS menu bar. There's no dock icon cluttering your workspace (unless the timeline window is open). From the menu bar you can:

- Open the timeline to review your day
- Pause and resume tracking
- Manually sync data to HeyGopher.ai
- Check for updates
- Toggle launch at login

### Automatic Tracking

Every 15 seconds, HeyGopher checks which application is in the foreground and what window is active. It records:

- **App name** — e.g. "Safari", "VS Code", "Slack"
- **Window title** — e.g. the browser tab title, document name, or channel you're viewing
- **Duration** — how long you stayed in that window
- **Idle status** — whether you stepped away from the keyboard

No screenshots are taken. No keystrokes are recorded. No screen content is captured.

### Idle Detection

If you step away from your Mac for more than 5 minutes (no mouse or keyboard input), HeyGopher marks that time as idle. This keeps your active hours accurate — a 2-hour lunch break won't inflate your screen time.

### Timeline View

The timeline shows your day as a series of color-coded blocks. Each block represents a time window (5, 15, or 30 minutes — your choice) and shows the app you spent the most time in during that period. Click any block to see a detailed breakdown of every app and browser tab you used in that window.

Features:
- **Date picker** to review any previous day
- **Search and filter** by app or window title
- **Zoom levels** — 5, 15, or 30-minute time buckets
- **Current time indicator** — a red line showing "now" on today's timeline
- **Hours active** — a running total of your active (non-idle) time for the day

### Privacy-First Design

HeyGopher is built with privacy as a core principle:

- **All data is stored locally** in a SQLite database on your Mac. Nothing leaves your computer unless you explicitly connect to HeyGopher.ai and sync.
- **Private browsing is automatically detected and redacted.** If you're in an incognito/private window in Safari, Chrome, Firefox, Brave, Edge, or Arc, the window title is replaced with "Private Browsing" before it's ever written to the database.
- **System screens are ignored.** The lock screen, screensaver, and security dialogs are treated as idle time, not tracked as app usage.

### Syncing to HeyGopher.ai

Syncing is optional. If you connect your HeyGopher.ai account:

- Click "Sync & Open in HeyGopher" to manually push your data, or enable auto-sync every 15 minutes
- Your activity data is sent to your private account on heygopher.ai
- Consecutive sessions in the same app/tab are merged so your timeline stays clean
- App icons are included so your web timeline looks just like the desktop one

### Browser-Aware Tracking

HeyGopher understands browsers. Instead of just showing "Safari — 2 hours", it breaks down your browser time by tab title. You can see exactly which websites and pages you spent time on (unless you were in private browsing, of course).

Supported browsers: Safari, Chrome, Firefox, Arc, Brave, Edge, Opera, Vivaldi, Orion, Zen Browser, and Chromium.

## Install

Download the latest DMG from [Releases](https://github.com/sponno/heygopher-desktop/releases), open it, and drag HeyGopher to your Applications folder.

**Requirements:** macOS 13 (Ventura) or later.

On first launch, macOS will ask you to grant **Screen Recording** permission. This is required so HeyGopher can read window titles — without it, only app names are captured. You can grant this in System Settings > Privacy & Security > Screen Recording.

## Signed and Notarized by Apple

This app is **code-signed** with an Apple Developer ID certificate and **notarized** by Apple. Here's what that means for you:

- **Code signing** guarantees the app hasn't been tampered with since it was built. macOS verifies the cryptographic signature every time the app launches. If anyone modified the binary — even a single byte — macOS would refuse to open it.

- **Apple notarization** means Apple has scanned the app for malware and known security issues before it was published. When you download HeyGopher, macOS checks with Apple's servers to confirm the app has been reviewed and approved for distribution. This is the same process used by apps distributed outside the Mac App Store.

Together, these mean you can download and open HeyGopher without seeing the "unidentified developer" warning, and you can trust that the app you're running is exactly what was built and reviewed.

## Auto-Updates

HeyGopher includes automatic update checking via [Sparkle](https://sparkle-project.org/). When a new version is available, you'll be prompted to update directly from the app. You can also check manually from the menu bar: **Check for Updates...**

All updates are cryptographically signed to ensure they haven't been tampered with.
