# Re-Tek corp. ..::77th JSOC::.. Server Tactical Monitor (STM) PRO V6.0

**STM PRO V6.0** is a browser-based tactical dashboard designed for quick monitoring of the **77th JSOC EU-1, EU-2, and EU-3** servers.

The system provides real-time server visibility, player tracking, squad roster tools, visual alerts, voice notifications, local persistence, and watchdog-style telemetry analysis. It is built as a static frontend application, making it easy to deploy through GitHub Pages without requiring a backend server.

Designed, tested, and directed by **Re-Tek**.  
Code implementation assisted by AI tools.

---

## ⚡ System Capabilities — V6.0 “Silent Hunter”

### 🛰️ Real-Time Server Uplink
Live monitoring for EU-1, EU-2, and EU-3, including player count, map/area of operations, latency, capacity status, and server availability.

### 🛡️ K.M.S. Watchdog V6.0 — Silent Hunter
Adaptive watchdog logic for tracking server stability and suspected restart events. Includes cooldown protection, cold-start handling, offline buffering, and additional checks designed to reduce false restart alerts.

### 🧠 Heuristics & Restart Detection
Analyzes uptime changes, population drops, mass disconnect patterns, veteran operator activity, and API instability signals to distinguish between normal player movement, BattleMetrics delay, API downtime, and probable server restart events.

### 📡 Radar Modes — ECO / NORM / AGR
Adjustable polling behavior depending on how actively the dashboard needs to monitor the servers.

- **ECO** — slower, lightweight monitoring
- **NORM** — balanced default monitoring
- **AGR** — aggressive refresh mode for active observation

### 🗣️ Voice Architect — TTS Engine
Customizable browser-based Text-to-Speech system with tactical voice feedback for important alerts and status changes.

### 🗄️ Persistent Operator Database
Local browser database using `localStorage` for squad assignments, tracked operators, session statistics, known players, watchdog state, and interface preferences.

### ⏱️ Active Stats Overlay
Optional roster statistics showing current session time and total historical tracked time for known operators.

### 🎯 AUTO-FAV Routing
Automatically detects new unlinked operators and routes them into the FAV squad for quick temporary tracking.

### 🟢 Server Saturation & Visual Telemetry
Live server capacity bars, population percentages, status indicators, neon-style trend graph, and mini oscilloscope-style latency visualization.

### ⚠️ DMD / VFD Tactical UI
Dynamic display system with priority messages, analysis states, restart alerts, server-full warnings, and high-visibility visual feedback.

### 🔍 Quick Intel Controls
Fast operator interaction tools, including double-click tracking, squad assignment, watchlist management, manual override controls, backup/export, and restore options.

---

## 🧩 Deployment

STM PRO V6.0 is designed to run as a static webpage.

Recommended deployment:

```text
/index.html
/Adobe Express - file.png
