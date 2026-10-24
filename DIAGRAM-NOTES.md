# What the scientific plates show (source-level notes)

Notes for the diagrams on this profile. Every curve is computed by code from the equations below; nothing is drawn by hand.

## The equation

The Schwarzschild metric, units G = c = 1:

  ds² = −(1 − r_s/r) dt² + (1 − r_s/r)⁻¹ dr² + r² dΩ²,  r_s = 2M.

The code works in units r_s = 2M = 1. Every radius quoted on a plate is converted back to M (r = 2M, r = 3.6M).

## Coordinates (Penrose diagram)

1. Kruskal–Szekeres null coordinates U, V, defined by UV = (1 − r) e^r and V/U = −e^t in region I (units 2M = 1).
2. Compactified: P = arctan U, Q = arctan V, each in (−π/2, π/2).
3. Screen: x = cx + s(Q − P), y = cy − s(Q + P). Radial light rays are lines at ±45°.

Regions: I (U < 0 < V) is the exterior; II (U, V > 0) the black-hole interior; III and IV are the mirror exterior and the white-hole interior of the *eternal* solution.

## What each line is

| Mark | Meaning | Status |
|---|---|---|
| Grid in region I | curves of constant r (17, crowding toward r = 2M) and constant t (27) | exact, sampled |
| Grid in region II | constant r (12) and constant t (27) inside the horizon; masked toward r = 0 only to show where the classical theory stops | exact, sampled; the fade is a drawing choice |
| Diagonals through the centre | the horizons U = 0 and V = 0, i.e. r = 2M | exact |
| Zigzag | r = 0, the curvature singularity (UV = 1, a straight edge after compactification) | exact |
| Dashed regions III and IV | present in the maximally extended (eternal) solution; **not part of a black hole formed by stellar collapse**, where the collapsing star replaces them | exact as mathematics; physically not expected |
| Thick curve | an observer falling radially from rest at r₀ = 2.5M (r₀ = 1.25 in code), exact geodesic (MTW eq. 31.10, cycloid parameter η) | exact; r₀ chosen |
| Thin curve on the right | a static receiver at r = 3.6M (1.8 in code) | exact; radius chosen |
| Ink rays | 16 outgoing radial light signals (U = const) emitted at equal steps of the faller's proper time; each runs from its emission event to where it meets the receiver | exact; the count 16 is chosen |
| Orange rays | the signals of those 16 emitted at or inside r = 2M; along U = const > 0 they reach r = 0 and never meet the receiver | exact (a property of the model) |

## The two annotations, stated precisely

- **"last of 16 to arrive"** labels the final *sampled* signal that meets the receiver. With continuous emission there is no last signal: emissions made ever closer to the horizon crossing arrive ever later, without bound.
- **"first of 16 sent inside r = 2M"** labels the first sampled emission that never arrives.

## Status vocabulary (V3)

A mathematical depiction is not an observation. Plates distinguish:

- **model** — computed from an equation (lines). Solid where the model describes black holes formed by collapse; dashed where it is eternal-solution only.
- **measured** — a number from a run (filled dots and bars).
- **registered** — a protocol frozen before a run (squares; hollow when not yet run).

The accent means "does not arrive / does not pass", and its form says which:

- on a **line**: a modelled signal the equations say can never reach the receiver;
- on a **bar or dot**: a measured result that **failed its preregistered gates**. This is scoped to that protocol and corpus; it is not a general falsification.

A measured result that merely went against expectation without a registered test (Layered-Memory-Architecture's MRR) is drawn in ink, not in the accent.
