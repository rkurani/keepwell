# Keepwell — Flows

Field-knowledge capture app for the Penn Water Center pilot. Pairs with Mentra Live glasses.
The one-liner: **capture the old head's know-how before he walks out the door, and hand it to the next hire.**

Live prototype: https://claude.ai/code/artifact/171622cb-b49d-48d2-9948-4cea07c940b3
Source: `/Users/ravikurani/Projects/mentra-water-demo/index.html`

---

## Two personas, one app (role toggle at top of Home)

- **Operator** (Frank, 34 yrs) — the person in the field who *uses* it.
- **Supervisor** (Sam, Operations) — the person who's *scared of losing Frank*. This is the pitch view.

---

## Screen map

```
Keepwell
├── Home ─ Operator          route, start capture, recent captures
├── Home ─ Supervisor        crew knowledge-at-risk dashboard
├── Capture (overlay)        live glasses feed → structured record
├── Session detail           the memorialized capture (Tips / Transcript / Assets)
├── Library                  global search across all captured knowledge
├── Assets                   list of assets + coverage
│   └── Asset health         utility-style telemetry + captured knowledge
└── Me                       operator profile (incl. retirement date)

Bottom nav: Home · Library · [Capture] · Assets · Me
```

---

## FLOW 1 — Operator captures (the signature moment)

**Goal:** turn a routine Frank has run 1,000 times into a structured, searchable record — without adding work.

1. **Operator Home** → "Morning, Frank," glasses connected 72%, today's route (Lift Station 4 up next).
2. Tap **Start capture** (or center nav button).
3. **Capture overlay** — full-screen glasses feed:
   - Detection boxes lock onto assets (Control Panel, Pump #2, Float Switch…).
   - Frank's speech types across the bottom as live captions.
   - When he drops know-how ("runs hot, normal since '09") → **★ Tip captured** toast.
   - He asks a question ("when'd we last rebuild #2?") → **grounded answer** card with a source (WO #4471 · O&M §4.3).
   - Live counter: *8 moments · 4 tips.*
4. **Stop** → "Session captured — 5 assets, 4 tips, 0:58."
5. **View session** → Session detail.

**Controls for the live demo:** play/pause, tag (+), close. Or jump straight in from the "Live capture" button under the phone.

---

## FLOW 2 — The capture becomes usable (memorialize)

**Goal:** prove the record is trustworthy and searchable, not a black box.

1. **Session detail** — "Lift Station 4 · Inspection · Frank M. · 0:58."
2. Chaptered player (Approach & Listen → Control Panel → Pump #2 → Floats & Amps → Wet Well).
3. Segmented control:
   - **Tips** — the 4 amber know-how nuggets (the gold).
   - **Transcript** — every moment (saw / said / did / asked), each timestamped.
   - **Assets** — what was detected, with counts.
4. Footer: **Share to crew** · **Add to training →.**

---

## FLOW 3 — Anyone finds what Frank knew (library)

**Goal:** the "type a word, get the veteran's answer" moment.

1. **Library** → search "everything the crew knows."
2. Type **float / hot / grease** (or tap suggestion chips).
3. Cards filter live, each sourced back to *Frank M. · Lift Station 4 · [chapter].*
4. Filter by Tips / Saw / Said / Did.

> This is the live-demo party trick — search in front of Penn and watch Frank's knowledge surface.

---

## FLOW 4 — Supervisor sees the risk (the pitch)

**Goal:** make the silver-tsunami problem *visceral* to utility management.

1. Toggle to **Supervisor** on Home.
2. **Crew knowledge dashboard:**
   - Gauge: **41% of crew knowledge captured.**
   - Headline: **"3 senior operators retire within 24 months."**
   - **Knowledge at risk** — operators listed with years, retirement flag, % captured (Frank: 34 yrs, ↓ Mar 2027, 62%).
   - **Coverage by asset** — bars per asset; Clearwell & Chlorine sits at a red **0% — no captures** (the visible gap).
3. CTA: **Schedule a capture with Frank →.**

---

## FLOW 5 — Asset health (utility telemetry skin)

**Goal:** operational credibility — speak the utility's data language, then layer knowledge on top.

1. **Assets → Lift Station 4** (or "Asset health" jump).
2. **Telemetry card:**
   - Radial **health ring (92)**, readout = *"Runtimes even, floats set right"* (Frank's own tell).
   - Stat pairs: P1 14.2A · P2 15.8A · 42 starts/day · 3.1h runtime.
   - **Day / Week / Month** toggle → live bar chart.
3. **Captured knowledge** block: *8 moments · 4 tips · 78% of Frank's routine captured* → Open full session.

> The point: the sensor data and Frank's judgment are looking at the same station.

---

## Held for next passes (from the Mobbin research)

- **Jobber field-service chrome** — bold job title + Directions + status pill + Schedule/Timesheet nav. Makes it feel like a tool operators already know.
- **Inspection step→verify loop** (Turo / N26) — reframe capture as a guided inspection with a post-capture *"confirm what Keepwell captured"* checklist. This is what makes an AI-generated record trustworthy for compliance — directly serves the agency/risk framing.
- **Glasses pairing / onboarding** — first-run flow connecting the Mentra device.
- **Handoff / Assist mode** — new hire (Maya) in the field, Frank's captured tips pushed to *her* HUD contextually. The knowledge-transfer completing, as a product screen.

---

## Open decisions

- **Name** — "Keepwell" is a placeholder. Brand as SWC product?
- **Split into files** — currently one `index.html`; can break into `index.html` / `styles.css` / `app.js` for a real repo start.
- **Primary demo path** for the Penn call — recommend: Supervisor dashboard (problem) → Live capture (solution) → Library search (payoff).
