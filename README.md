# WisdomLine 📞

**Retired experts. Busy juniors. One phone call apart.**

*Independence Day Hackathon 2026 — Voice AI track*

---

## The problem

Retired professionals hold decades of hard-won, practical knowledge — but have no structured way to share it. Juniors and busy people need that guidance constantly (career decisions, negotiation, a trade skill, life advice) but rarely have a mentor network and don't have time to search for one.

Most "mentorship platforms" also assume both sides are comfortable with an app, an account, and a scheduling flow — which quietly excludes the very seniors who have the most time and willingness to help, but the least patience for software. And even when a conversation does happen, the wisdom shared disappears the moment the call ends — nobody else ever benefits from it again.

## The solution

WisdomLine is a **voice-only, phone-call-based agent** — no app required on either side.

- A **junior** calls in, describes in plain speech what they need help with, and is instantly matched by an AI reasoning layer to the retired mentor whose real background best fits — then hears that mentor's specific, first-person advice, spoken back to them.
- A **retired person** can just as easily call in and describe what they've spent their life getting good at, by voice, in two sentences, to join the mentor pool.
- The key differentiator: **every call is automatically distilled into a short, tagged "knowledge card"** and saved into a permanent, searchable Wisdom Library — so the next person with a similar question benefits from that mentor's experience without needing to make a call at all. One conversation becomes reusable, compounding value instead of a one-off exchange.

## Try it

Open `wisdomline_demo.html` in Chrome (needed for voice input):

1. Choose **"I need guidance"** or **"I want to mentor."**
2. Tap the mic and just talk — or use the text box if you'd rather type.
3. Watch the AI match you to a mentor persona, speak back real advice, and drop a new card into the **Wisdom Library** below.

No signup, no install — it's the same interaction model a real phone call would be.

## How it works

```
Voice input (browser mic, standing in for a real phone line)
        │
        ▼
AI matching engine — reasons over mentor roster, picks best fit
        │
        ▼
Mentor's first-person response generated + spoken back (text-to-speech)
        │
        ▼
Knowledge card auto-extracted → saved to the shared Wisdom Library
```

In production, the browser mic/speaker layer is replaced by a real telephony connection (carrier or VoIP API) — the matching, reasoning, and knowledge-capture logic already built doesn't change.

## Why it's different

Existing mentorship platforms are text-and-profile based, which filters out exactly the senior population with the most to offer and the least tolerance for app friction. WisdomLine is voice-first *because* accessibility is the whole design, not a workaround — and treating each call as a knowledge-capture event, not just a live conversation, turns a fundamentally unscalable resource (a retired person's limited hours) into a compounding, searchable asset.

## Tech stack

- **Web Speech API** — voice input (SpeechRecognition) and output (SpeechSynthesis) in-browser
- **Claude (claude-sonnet-4-6)** via the Anthropic API — mentor matching, first-person response generation, knowledge-card extraction, mentor-profile structuring
- **Persistent shared storage** — the Wisdom Library, so cards accumulate across sessions/users

## Who this is for

| Buyer | Why |
|---|---|
| Senior-living / retiree communities | Engagement and purpose for residents |
| Universities & bootcamps | Alumni mentorship at scale |
| Corporate L&D teams | Cross-generational knowledge transfer before retirement-driven knowledge loss |
| Community / immigrant-services orgs | Serving populations underserved by typical apps |

## Files in this repo

- `wisdomline_demo.html` — the full working demo (single file, no build step)
- `WisdomLine_OnePager.pdf` — one-page problem/solution/impact summary
- `README.md` — this file

---

*Built for the Independence Day Hackathon 2026.*
