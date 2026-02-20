# SKILL: TRAC COMBAT — AI Fighter Agent

## Overview
This skill enables an Intercom/IntercomSwap agent to operate the TRAC COMBAT fighting game, manage sessions, report outcomes, and interface with the TRAC/TAP Protocol for reward distribution.

## Agent Capabilities

### 1. Launch Combat Session
The agent can initialize a combat match:
- Open `index.html` in a browser context
- Trigger the "INITIALIZE COMBAT" button
- Monitor player HP, AI HP, round number, and timer

### 2. Match State Reporting
After each round/match, report:
```json
{
  "match_id": "<uuid>",
  "round": 1,
  "player_hp_final": 45,
  "ai_hp_final": 0,
  "winner": "player",
  "duration_seconds": 38,
  "trac_address": "YOUR_TRAC_ADDRESS_HERE"
}
```

### 3. Combat Instructions
The agent should advise human players:
- Use `J` (punch) for fast low-damage attacks
- Use `K` (kick) for medium damage with knockback
- Use `L` (TRAC Special) when energy bar is full (gold bar above head)
- Use `U` (block) when AI is attacking at close range
- Jump (`W`) to dodge sweeping kicks

### 4. AI Behavior Awareness
The agent knows the AI state machine:
- When AI HP < 30%, it enters AGGRESSIVE mode — increase blocking
- AI makes attack decisions every 8-20 frames
- Keep distance > 150px to force AI into APPROACH mode (easier to counter)

### 5. Reward Integration
On match completion, the agent can:
- Verify winner via DOM state (`#playerScore`, `#aiScore`)
- Submit match proof to TAP Protocol endpoint
- Request TNK/TRAC payout to the registered TRAC address

## Usage Example

```
User: "Start a TRAC combat match"
Agent: Opens index.html, clicks INITIALIZE COMBAT, monitors game state

User: "How do I beat the AI?"
Agent: "Use TRAC Special (L key) when your energy bar is full. Keep distance 
        and punish when AI is in RETREAT state (HP below 30%)."

User: "I won 2-0, claim my reward"
Agent: Reports match data to TAP Protocol, references TRAC address for payout
```

## Technical Notes
- Game runs entirely in browser, no server required
- All state accessible via DOM: `#playerHpText`, `#aiHpText`, `#playerScore`, `#aiScore`
- Canvas ID: `#gameCanvas` (800x350 base resolution, responsive)
- No external dependencies — pure HTML/CSS/JS

## TRAC Address
`YOUR_TRAC_ADDRESS_HERE`
