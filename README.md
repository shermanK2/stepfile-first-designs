# First designs — STEP files

Wing and tail designs for small RC aircraft, exported as STEP files for manufacturing.
Each design iteration is kept in its own folder so earlier versions stay available and
comparable.

## Layout

```
<aircraft>/
├── README.md                    aircraft reference data (published specs, measurements)
└── v<N>-<YYYY-MM-DD>/           one folder per design iteration
    ├── README.md                design notes: parameters, dimensions, results, status
    ├── wing/                    main wing
    ├── tail/                    horizontal tail (hstab) and fin (vstab)
    └── assembly/                full aircraft, for fit checks only — not for cutting
templates/
└── design-notes.md              copy this into each new iteration folder
```

## Iterations

| Aircraft | Version | Date | Summary | Status |
|---|---|---|---|---|
| [Kavan Beta 1400](kavan-beta-1400/) | [v1](kavan-beta-1400/v1-2026-09-28/) | 2026-09-28 | Trapezoidal wing (AR 8, taper 0.6, 3° dihedral), conventional tail | Designed, not built |

## Conventions

- **Units:** every STEP file is in **millimetres**.
- **File names:** `<part>_mm.step`, e.g. `wing_mm.step`, `hstab_mm.step`, `fin_mm.step`.
- **Versions are never edited after they are sent to manufacturing.** A change means a new
  folder (`v2-…`), not an overwrite. Small fixes before anything is sent can stay in the
  same version; note them in its README.
- **Coordinates:** x = chordwise (aft positive), y = spanwise, z = up. Separate part files
  are in the part's own frame; the assembly file is in aircraft coordinates.

## Adding a new iteration

1. Create `<aircraft>/v<N>-<YYYY-MM-DD>/` with `wing/`, `tail/` and `assembly/` inside.
2. Copy the new STEP files in. Check each one opens at the expected size in mm.
3. Copy [`templates/design-notes.md`](templates/design-notes.md) to the new folder as
   `README.md` and fill it in, including **what changed since the previous version**.
4. Add a row to the **Iterations** table above.
5. Commit with a message like `Kavan Beta 1400 v2: <what changed>`.

## Tooling

The designs are generated with AeroForge (IDEAL Lab, ETH Zürich). The design scripts
live with the lab's AeroForge repository and are not included here.
