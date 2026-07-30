# Arithmetic and harmonic realizations of the Clebsch cubic

[![DOI](https://zenodo.org/badge/1316332661.svg)](https://doi.org/10.5281/zenodo.21682515)

**Series:** *The Clebsch cubic: recovering, orienting, and realizing --- III*

This directory contains the `clebsch-passages` manuscript and artifact.  Its
main theorem has two legs:

1. the rational square class of Hitchin's incidence cover, its exact local
   golden fibre, and the specialization of the fibre exchanger modulo `11`;
2. the degree-six icosahedral Gaunt/Steinhardt cubic on the Petersen
   four-space.

The fixed-icosahedron Clebsch charts in the first theorem are conjugate
charts over `Q(sqrt(5))`; they are not presented as rational subspaces of
the standard rational harmonic space.

## Source

- `clebsch_passages.tex`: manuscript driver.
- `sections/`: one file for each mathematical stage.
- `ARTIFACT.md`: stable artifact description and trust boundary.
- `release_files.json`: public packaging allowlist.
- `verification/trust_manifest.json`: claim/evidence/status ledger.
- `verification/statement_identity.json`: frozen theorem surface.
- `verification/verify_release.py`: aggregate release gate.

Build from this directory:

```text
make -B
```

Check the manuscript and complete trust surface:

```text
python3 verification/verify_release.py
```

The mod-\(11\) assertion concerns the displayed golden fibre and its
integral exchanger.  It does not assert that the full geometric incidence
comparison has good reduction at \(11\).

## Optional Lean formal companion

The separately released
[`finitegeom`](https://github.com/tavisrudd/finitegeom) library contains
kernel-checked proofs of two neighboring symbolic mechanisms:

- localized splitting of an involutive algebra by an odd unit; and
- the equivalence between the sum-zero five-vertex module and the Petersen
  graph's four-dimensional minus-two eigenspace.

The exact source revision and gate are recorded in `FORMAL_COMPANION.json`
and locked by `flake.lock`. The version-independent archival locator is the
Zenodo concept DOI
[`10.5281/zenodo.21650878`](https://doi.org/10.5281/zenodo.21650878). These
results are not premises of the manuscript's four claim groups. In
particular, they do not formalize the `5J₀` square class, golden fibre, spinor
specialization, face-axis geometry, spherical moments, or Gaunt coefficient.
