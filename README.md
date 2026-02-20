# ⬡ TRAC COMBAT — AI Agent vs Human Arena

> **A fork of [Intercom](https://github.com/Trac-Systems/awesome-intercom) | Built on TAP Protocol | Powered by TRAC Ordinals**

![TRAC Combat](https://img.shields.io/badge/TRAC-ORDINALS-f0b429?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHZpZXdCb3g9IjAgMCAyMCAyMCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cG9seWdvbiBwb2ludHM9IjEwLDEgMTksMTkgMSwxOSIgZmlsbD0iI2YwYjQyOSIvPjwvc3ZnPg==)
![Status](https://img.shields.io/badge/STATUS-MAINNET_LIVE-00ff88?style=for-the-badge)
![License](https://img.shields.io/badge/LICENSE-MIT-blue?style=for-the-badge)

---

<img width="1302" height="835" alt="image" src="https://github.com/user-attachments/assets/d87929ce-4ef9-4870-994a-f2d150d3f013" />


<img width="443" height="114" alt="image" src="https://github.com/user-attachments/assets/2cdf1170-2140-4151-b013-bf60a3e9a54b" />


<img width="1322" height="819" alt="image" src="https://github.com/user-attachments/assets/172d4328-0e49-4d02-8be6-32739406d0f1" />


## 🎮 About TRAC COMBAT

**TRAC COMBAT** is an AI-powered stickman fighting game built as a fork of the [Intercom protocol](https://github.com/Trac-Systems/awesome-intercom). Players battle against an AI agent in a real-time 2D fighting arena — fully themed around the **TRAC Ordinals ecosystem**.

This app demonstrates how AI agents can be integrated into interactive dApps built on Bitcoin Ordinals via the TAP Protocol.

### ✨ Features

- 🤖 **AI Agent Fighter** — Adaptive AI opponent powered by state-machine logic that evolves its attack patterns
- ⚡ **Special Moves** — Energy-based TRAC special attacks with particle effects
- 🛡️ **Block System** — Strategic blocking reduces damage by 80%
- 🎯 **Combo System** — Chain punches, kicks, and specials for maximum damage
- 📱 **Mobile Ready** — Touch controls for on-the-go TRAC combat
- 🌐 **Pure Frontend** — No server, no dependencies, runs entirely in-browser
- 🎨 **TRAC Branded** — Full TRAC/TAP Protocol visual identity

---

## 💰 TRAC Address

> **My TRAC Address for Payout:**  
> `trac1tfawevj77j0rqgdqp6mnygak8a3wc4cf8z6l6j6g6s67h902xwts28uqch`

*(Replace with your actual TRAC/Bitcoin Ordinals address)*

---

## 🚀 How to Run

### Option 1: Direct (Fastest)
```bash
# Just open in browser — zero dependencies!
open index.html
```

### Option 2: Local Server
```bash
npx serve .
# or
python3 -m http.server 8080
```

Then go to `http://localhost:8080`

---

## 🎮 Controls

| Action | Key |
|--------|-----|
| Move Left | `A` or `←` |
| Move Right | `D` or `→` |
| Jump | `W` or `↑` |
| Punch | `J` |
| Kick | `K` |
| **Special (TRAC Strike)** | `L` |
| Block | `U` |

**Mobile:** Touch buttons appear automatically on small screens.

---

## 🤖 AI Agent Behavior

The AI opponent (`AGENT.TRAC`) runs a dynamic state machine:

| State | Trigger | Behavior |
|-------|---------|----------|
| `APPROACH` | Distance > 150px | Moves toward player aggressively |
| `ATTACK` | Distance < 80px | Executes random punch/kick/special combo |
| `RETREAT` | HP < 30% | Falls back, increases blocking |
| `CIRCLE` | Mid-range | Lateral movement + random attacks |
| `AGGRESSIVE` | Low HP gambit | Ignores defense, pure offense |

The AI makes decisions every 8–20 frames with randomized variance, preventing exploitable patterns.

---

## 🏗️ Built on TAP Protocol

This app is designed to integrate with the **TAP Protocol** ecosystem:

- **TRAC token** recognition for reward events
- **Ordinals wallet** connection ready (extend with `ord-connect`)
- Agent logic mirrors real AI agent interactions on-chain
- Themed around the TRAC/TAP dApp ecosystem

### Integration Points (extend this fork):
```javascript
// Connect to TAP Protocol for real rewards
// window.unisat / xverse wallet integration
// Log match results as Ordinals inscriptions
// On-chain leaderboard via TAP taps
```

---

## 📂 File Structure

```
/
├── index.html        # Complete game (single file, zero deps)
├── SKILL.md          # Agent skill file for Intercom integration
└── README.md         # This file
```

---

## 🔧 SKILL.md — Agent Instructions

See [`SKILL.md`](./SKILL.md) for the full Intercom agent skill specification. The agent can:
- Launch and manage combat sessions
- Report match outcomes
- Interface with TRAC wallet for reward payouts
- Generate match replays

---

## 📸 Proof It Works

Open `index.html` in any modern browser. The game:
1. ✅ Loads instantly with zero installation
2. ✅ Shows TRAC-branded combat arena
3. ✅ Player controls respond immediately
4. ✅ AI opponent actively fights back
5. ✅ HP bars, round counter, and score all update live
6. ✅ Match ends with win/loss screen and rematch option

---

## 🔗 Links

- [TRAC / TAP Protocol](https://trac.network)
- [Intercom (Original)](https://github.com/Trac-Systems/awesome-intercom)
- [TAP Protocol Docs](https://github.com/Trac-Systems/tap-protocol)

---

*Built with ❤️ for the TRAC Ordinals ecosystem. Fork it, extend it, earn TNK.*
