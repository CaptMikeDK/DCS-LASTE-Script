# DCS Lua Scripts — CaptMikeDK

A collection of DCS World server-side Lua scripts built for multiplayer missions.  
All scripts require the [MOOSE Framework](https://github.com/FlightControl-Master/MOOSE) — download it from the link before adding any script to your mission.

---

## 📁 Scripts

### 🛩️ LASTE Wind/Temp Correction — A-10C / A-10C II

In an A-10C / A-10C II Thunderbolt, LASTE stands for Low Altitude Safety and Targeting Enhancement

**File:** `A10_laste_Winds_MP.lua`  
**Version:** 1.3 | 14-06-2026  

In an A-10 Thunderbolt II, LASTE stands for **Low Altitude Safety and Targeting Enhancement**.

This script pulls live in-mission weather data directly from the pilot's aircraft position and formats it ready to type straight into the CDU scratchpad — no math, no conversion needed.

#### Features
- Winds and temps at all 4 CDU altitude tiers (00, 02, 08, 26)
- Wind output pre-formatted as 5-digit strings (e.g. `08001`)
- Live QNH in inHg for your altimeter
- Local magnetic variation for the theatre
- Per-pilot display — MP safe, blue coalition only
- Built-in step-by-step CDU entry guide in the readout
- F10 menu driven — request or clear on demand

#### Requirements
- [MOOSE Framework](https://github.com/FlightControl-Master/MOOSE)

#### Mission Editor Setup
1. Create a trigger: **TYPE:** Mission Start → **ACTION:** Do Script File → select `Moose.lua`
2. Create a trigger: **TYPE:** Once → **CONDITION:** Time More (5) → **ACTION:** Do Script File → select `A10_laste_Winds_MP.lua`

#### In-Game Usage
`F10 Other` → `LASTE` → `Request LASTE Winds`

---

## License

Free to use and modify for non-commercial DCS mission development.  
Credit appreciated but not required.

