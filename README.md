# DCS Lua Scripts — CaptMikeDK

A collection of DCS World server-side Lua scripts built for multiplayer missions.  
All scripts require the [MOOSE Framework](https://github.com/FlightControl-Master/MOOSE) — download it from the link before adding any script to your mission.

---

## 📁 Scripts

### 🛩️ LASTE Wind/Temp Correction — A-10C / A-10C II

![LASTE Wind/Temp Correction Data](A-10_laste.jpg)

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

MIT License

Copyright (c) 2026 CaptMikeDK

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
