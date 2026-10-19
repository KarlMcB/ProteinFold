# ProteinFold

An interactive, single-file web lab where high school biology students build a protein
from polar and nonpolar amino acids and watch it fold in 3D.

**Run it:** open `index.html` in any modern browser. No install, no internet needed
(works on Chromebooks, laptops, tablets).

## What students do
1. **Build & Fold**: choose the order of polar (blue) and nonpolar (orange) amino acids,
   predict where each type will end up, then watch the chain collapse. Drag to rotate, hover for the
   amino acid's name, switch between a watery cell and an oily membrane, and hold *Heat* to
   denature the protein and watch it refold on cooling.
2. **Mutation Lab**: compare a normal β-globin fragment with a mutant (sickle-cell swap, or any swap).
3. **Worksheet**: runs and predictions are logged automatically; print/save as PDF or copy as text.

Six challenges (hide the oily parts, fully buried, inside-out membrane protein, sticky patch,
zipper test, sticky-swap detective) give students goals.

## Science notes
- The model captures the **hydrophobic effect** only: cluster-type beads attract each other and
  the others are pushed to the surface. Exposure is a Shrake–Rupley-style solvent-accessibility estimate.
- It does not model hydrogen bonds, ionic bonds, disulfides, or chaperones, and it cannot predict
  real protein structures. Folding includes randomness, so results vary between runs.
- Relevant standard: NGSS HS-LS1-1 (structure of proteins and how it relates to function).

## Development
All code lives in `index.html`. The physics is between the `==SIM-START==` / `==SIM-END==` markers
so it can be unit-tested in Node.
