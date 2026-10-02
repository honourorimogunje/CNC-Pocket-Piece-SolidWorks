# CNC Pocket Piece — SolidWorks

A parametric solid model of a pocketed aluminium-style plate with six countersunk fastener holes, built in SolidWorks as part of **MECH 2112 — Fundamentals of Mechanical and Computer Aided Design** at the University of Manitoba.

The part geometry and dimensions were supplied by the course; the modelling, feature strategy and documentation in this repository are mine.

---

## The part

A rectangular plate with a shallow machined pocket whose long sides are scalloped by six large-radius arcs, and six countersunk through-holes positioned around the perimeter.

| Property | Value |
|---|---|
| Overall footprint | 114.2 × 64 mm |
| Plate thickness | 12 mm |
| Pocket depth | 4 mm |
| Pocket corner fillets | 12 × R1 |
| Pocket scallop radii | 6 × R12.5 |
| Fastener holes | 6 × Ø2.38 through |
| Countersinks | Ø5.86 × 82° |
| Hole pitch (long axis) | 50.7 mm |
| Hole inset from edges | 6.4 mm |
| Units / template | Millimetres, ISO part template |

The 82° countersink angle matches standard inch-series flat-head fasteners, so the hole pattern is sized for a specific screw family rather than drawn to arbitrary numbers.

---

## Modelling approach

The model is built as a short, readable feature tree rather than a single complex sketch:

1. **Extruded Boss/Base** — centre rectangle sketched on the Top Plane, dimensioned 114.2 × 64 and extruded to 12 mm. Sketching from the part origin with a centre rectangle keeps the part symmetric about both planes, which makes every later feature easier to locate.
2. **Extruded Cut** — pocket profile with the six R12.5 scallops, cut to 4 mm depth.
3. **Fillets** — 12 × R1 on the pocket corners.
4. **Hole Wizard** — six countersunk holes, Ø2.38 through with Ø5.86 × 82° countersinks.

**Every sketch is fully defined.** No under-defined geometry remains in the tree, so dimensions drive the model rather than drag-and-drop placement — change a value and the part updates predictably.

---

## Repository contents

```
├── cad/
│   ├── CNC_Pocket_Piece.SLDPRT     # native SolidWorks part
│   └── CNC_Pocket_Piece.step       # neutral format, opens in any CAD package
├── drawings/
│   └── CNC_Pocket_Piece.pdf        # dimensioned drawing
└── renders/
    └── isometric.png               # shaded isometric view
```

---

## Opening the files

**With SolidWorks** — open `cad/CNC_Pocket_Piece.SLDPRT` directly. Built in SolidWorks 2025; older versions will not open it, so use the STEP file instead.

**Without SolidWorks** — `cad/CNC_Pocket_Piece.step` opens in Fusion 360, Onshape, FreeCAD, Inventor, CATIA and most other packages. The STEP carries the geometry but not the feature history.

---

## What this demonstrates

- Building a part from a dimensioned multiview drawing rather than from a picture
- Fully defined sketches and a deliberate feature order
- Hole Wizard for standards-based fastener features instead of hand-drawn cylinders
- Reading and working to a sectioned engineering drawing

---

## Author

**Honour Orimogunje** — Mechanical Engineering, University of Manitoba
[LinkedIn](https://www.linkedin.com/in/honourorimogunje/)
