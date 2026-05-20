# Re-Tek corp. ..::77th JSOC::.. Server Tactical Monitor (STM) PRO V6.0

**STM PRO V6.0** is a browser-based tactical monitoring dashboard designed for quick observation of the 77th JSOC EU-1, EU-2, and EU-3 servers.

The system provides live server visibility, player tracking, squad roster tools, visual alerts, voice notifications, local persistence, restart telemetry, and watchdog-style server analysis. It is built as a static frontend application, making it easy to deploy through GitHub Pages without requiring a backend server.

Designed, tested, and directed by **Re-Tek**.  
Code implementation assisted by AI tools.

---

## ⚡ System Capabilities — V6.0 “Silent Hunter”

### 🛰️ Real-Time Server Uplink

Live monitoring for **EU-1**, **EU-2**, and **EU-3**, including:

- player count
- current map / area of operations
- latency
- slot capacity
- online / offline / booting state
- full-server warnings

---

### 🛡️ K.M.S. Watchdog V6.0 — Silent Hunter

Watchdog-style telemetry layer for tracking server stability, restart events, and server availability.

The watchdog monitors live API responses, server state changes, server identity changes, latency behavior, and player movement patterns to determine whether a server is stable, restarting, offline, or recovering.

---

### 🔁 Deterministic Restart Detection

Primary restart detection is based on **BattleMetrics `serverSteamId` rotation**.

When the game server process restarts, Steam re-registers the server and assigns a new server identity. STM compares the current `serverSteamId` against the previously stored value and treats a change as a confirmed restart event.

Restart detection hierarchy:

1. **serverSteamId rotation** — primary deterministic restart signal
2. **details.time / uptime reset** — fallback for games that expose uptime
3. **confirmed API dead/offline samples**
4. **mass-disconnect and latency-based heuristic fallback**

After a confirmed restart, the server roster is cleared immediately and players are only shown again once they reconnect after the restart.

---

### 📡 Radar Modes — ECO / NORM / AGR

Adjustable monitoring behavior depending on how actively the dashboard needs to observe the servers.

- **ECO** — slower, lightweight monitoring
- **NORM** — balanced default monitoring
- **AGR** — aggressive refresh mode for active observation and testing

---

### 🗣️ Voice Architect — TTS Engine

Browser-based Text-to-Speech system with tactical voice feedback for important alerts and status changes.

Includes:

- voice selection
- mute / volume controls
- join / leave notifications
- server restart alerts
- full-server warnings
- audio queue protection for improved stability

---

### 🗄️ Persistent Operator Database

Local browser persistence using `localStorage`.

STM stores:

- squad assignments
- tracked operators
- session statistics
- total historical tracked time
- watchdog state
- restart history
- radar mode
- interface preferences

All data is stored locally in the user’s browser.

---

### ⏱️ Active Stats Overlay

Optional roster statistics showing:

- current session time
- total historical tracked time
- operator activity
- squad presence

---

### 🎯 Squad Tracking & AUTO-FAV Routing

Operators can be grouped into tactical squads:

- ALFA
- BRAVO
- CHARLIE
- DELTA
- ECHO
- FOXTROT
- GOLF
- FAV

New unlinked operators can be drafted or automatically routed into the FAV squad for quick temporary tracking.

---

### 🟢 Server Saturation & Visual Telemetry

Live visual telemetry includes:

- capacity bars
- population percentages
- online/offline indicators
- server-full warnings
- global population counter
- population trend graph
- mini oscilloscope-style latency/player graphs

---

### ⚠️ DMD / VFD Tactical UI

Dynamic tactical display system with:

- priority alerts
- restart warnings
- server-full messages
- watchdog analysis states
- API heat display
- clock display
- visual status transitions

---

### ⏱️ Restart Clock System

Each server has a restart clock showing time since the last detected restart.

The clock can switch between:

- elapsed time since last restart
- last known restart time

Manual override is available for correcting approximate restart time when needed.

---

### 🧰 Quick Intel Controls

Fast operator and system tools include:

- double-click player tracking
- squad assignment
- local watchlist management
- manual restart-time override
- database export
- system backup
- restore
- local memory reset
- blackbox log export

---

## 🧩 Deployment

STM PRO V6.0 is designed to run as a static webpage.

Recommended deployment:

```text
/index.html
/Adobe Express - file.png
