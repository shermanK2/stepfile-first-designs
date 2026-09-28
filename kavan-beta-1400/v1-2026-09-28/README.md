# Kavan Beta 1400 — v1 (2026-09-28)

First trapezoidal wing and conventional tail designed around the Kavan Beta 1400 fuselage.

**Status:** designed, not yet built or flown.
**Changes from previous version:** none — first version.

## Files

| File | Part | Size (x × y × z, mm) |
|---|---|---|
| [`wing/wing_mm.step`](wing/wing_mm.step) | Main wing, one piece tip to tip | 218.8 × 1400.0 × 56.3 |
| [`tail/hstab_mm.step`](tail/hstab_mm.step) | Horizontal tail | 131.3 × 420.0 × 15.8 |
| [`tail/fin_mm.step`](tail/fin_mm.step) | Fin (exported lying flat, height along y) | 168.9 × 190.0 × 20.3 |
| [`assembly/aircraft_fitcheck_mm.step`](assembly/aircraft_fitcheck_mm.step) | Full aircraft — fit check only | 1034.7 × 1400.0 × 303.5 |

All files are in millimetres.

## Design parameters

| Part | Span | Aspect ratio | Taper | Thickness | Sweep | Dihedral | Airfoil |
|---|---|---|---|---|---|---|---|
| Wing | 1400 mm | 8.0 | 0.6 | 12 % | 0° | 3° | NACA 2412 |
| Horizontal tail | 420 mm | 4.0 | 0.6 | 10 % | 0° | 0° | NACA 0012 |
| Fin | 190 mm (height) | 1.5 | 0.5 | 10 % | 0° | — | NACA 0012 |

## Derived dimensions

| | Wing | Horizontal tail | Fin |
|---|---|---|---|
| Area | 0.2450 m² | 0.0441 m² | 0.0241 m² |
| Mean chord | 175.0 mm | 105.0 mm | 126.7 mm |
| Root chord | 218.8 mm | 131.3 mm | 168.9 mm |
| Tip chord | 131.3 mm | 78.8 mm | 84.4 mm |
| Mean aerodynamic chord (MAC) | 178.6 mm | | |

Tail volume coefficients (tail arm 599 mm): horizontal **0.62**, vertical **0.042** —
both in the usual trainer range (0.45–0.65 and 0.035–0.05).

## Fuselage and placement used

| | Value | Source |
|---|---|---|
| Fuselage length | 966 mm | Published |
| Fuselage width × height | 150 × 140 mm | **Placeholder** |
| Wing ¼-root-chord position | 30 % of length (290 mm from nose) | **Placeholder** |
| Tail ¼-root-chord position | 92 % of length (889 mm from nose) | **Placeholder** |

The fit-check assembly uses these placeholders, so it is approximate until they are measured.

## Predicted performance (AeroForge handbook models)

| | Value | Notes |
|---|---|---|
| Flying weight used | 0.737 kg | Tuned to the published 700–770 g |
| Stall speed | 6.2 m/s | Fixed CLmax 1.3 — rough |
| Best L/D | 13.0 | At ~7.8 m/s |
| Spar safety factor | 6.4 | 8/6 mm carbon tube, 3 g, tube carries all load |
| Wing tip deflection | 25 mm | At 3 g |

Conditions: cruise 13 m/s, altitude 450 m.

## Manufacturing notes

- **Wing is one solid piece** (1.4 m) with **no spar slot**. Decide whether to split it at
  the root.
- **Spar:** planned as an 8 mm OD / 6 mm ID carbon tube at the root quarter-chord. A single
  straight tube will exit the wing near the tips because of the 3° dihedral (tip is ~16 mm
  thick but ~37 mm higher) — use **two half-spars joined with a dihedral brace**.
- **Fin** is exported lying flat; it is the vertical fin.
- **Incidence** is not included in the geometry; set it when mounting.
- **Balance** at 25–30 % MAC: **45–54 mm behind the wing leading edge**, nose-heavy end
  first.
- The assembly file contains ~15 separate bodies and is for reference only.

## Open items for v2

- [ ] Measure fuselage width, height and the wing and tail mount positions.
- [ ] Weigh the real components and update the mass.
- [ ] Decide wing split and spar joint.
- [ ] Record build and flight results here.
