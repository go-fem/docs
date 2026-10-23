---
title: "mms"
weight: 20
description: "The shared method-of-manufactured-solutions convergence harness."
---

<!-- From go-scikit/roadmap PLAN.md and bib/geometry-pde-graphs.md (section 2, algorithms; section 3, implementations; section 4, validation). The package has no repository yet: change the roadmap first, then here. -->

**Status: planned (wave 3).** There is no repository and no code yet, and `mms` is a working name. These pages describe the plan, not a release.

The shared method-of-manufactured-solutions convergence harness.

## What it will provide

| | |
|---|---|
| harness | pick an exact solution, derive the source term and boundary data, run a refinement sequence, and report the observed convergence order |
| use | the test kit of the other packages of the organization, and of anyone validating a PDE solver |

## References

The algorithms and the theory the package will start from, as the roadmap's bibliography lists them:

| Reference | Cite |
|---|---|
| Brenner, Scott, The Mathematical Theory of Finite Element Methods, Springer (the a priori error estimates it checks) | doi:10.1007/978-0-387-75934-0 |

## Reference implementations and licences

What exists, under which licence, and what that allows:

| Implementation | Licence and use |
|---|---|
| no external corpus | the method needs none: the exact solution is chosen |

GPL, LGPL, AGPL and non-free code is never ported: it is only run as an oracle, as an external program.

## How it will be validated

- The harness is itself tested on a problem whose convergence order is known, so that a wrong order is reported as wrong.

## Depends on

nothing; it is small and independent, and is listed first in the plan's priorities.

## Scope notes

Two further items sit at the lowest priority in the plan and are not scheduled: a one-dimensional method of lines (a pdepe analogue over go-numerics/integrate) and finite differences and volumes on structured grids.

## Where the plan lives

[PLAN.md](https://github.com/go-scikit/roadmap/blob/main/PLAN.md), [STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md) and the [bibliography](https://github.com/go-scikit/roadmap/blob/main/bib/geometry-pde-graphs.md) in the go-scikit roadmap.
