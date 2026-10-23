---
title: "fem"
weight: 10
description: "Lagrange finite elements, quadrature, assembly, boundary conditions and the first PDE solvers."
---

<!-- From go-scikit/roadmap PLAN.md and bib/geometry-pde-graphs.md (section 2, algorithms; section 3, implementations; section 4, validation). The package has no repository yet: change the roadmap first, then here. -->

**Status: planned (wave 3).** There is no repository and no code yet, and `fem` is a working name. These pages describe the plan, not a release.

Lagrange finite elements, quadrature, assembly, boundary conditions and the first PDE solvers.

## What it will provide

| | |
|---|---|
| elements | Lagrange P1 and P2 on triangles |
| quadrature | tabulated symmetric Gauss rules on the triangle |
| assembly | stiffness and mass matrices assembled into go-sparse containers, with Dirichlet, Neumann and periodic boundary conditions |
| equations | Poisson first, then heat, wave and elasticity; Stokes later |

## References

The algorithms and the theory the package will start from, as the roadmap's bibliography lists them:

| Reference | Cite |
|---|---|
| Brenner, Scott, The Mathematical Theory of Finite Element Methods, Springer | doi:10.1007/978-0-387-75934-0 |
| Ern, Guermond, Theory and Practice of Finite Elements, Springer, 2004 | doi:10.1007/978-1-4757-4355-5 |
| Logg, Mardal, Wells (eds.), Automated Solution of Differential Equations by the Finite Element Method, Springer, 2012 | doi:10.1007/978-3-642-23099-8 |
| Dunavant, High degree efficient symmetrical Gaussian quadrature rules for the triangle, IJNME 21(6):1129-1148, 1985 | doi:10.1002/nme.1620210612 |
| Xiao, Gimbutas, A numerical algorithm for the construction of efficient quadrature rules in two and higher dimensions, Comput. Math. Appl. 59(2):663-676, 2010 | doi:10.1016/j.camwa.2009.10.027 |
| LeVeque, Finite Volume Methods for Hyperbolic Problems, CUP, 2002 (for the finite-volume work the plan lists at lower priority) | doi:10.1017/CBO9780511791253 |

## Reference implementations and licences

What exists, under which licence, and what that allows:

| Implementation | Licence and use |
|---|---|
| MFEM | BSD-3-Clause; a clean design reference for elements and assembly |
| deal.II | Apache-2.0 with LLVM exception on one side, LGPL-2.1+ on the other: the Apache side may be ported after checking each file's SPDX header |
| FEniCS / DOLFINx | LGPL-3.0: an oracle only, on a Linux lane |

GPL, LGPL, AGPL and non-free code is never ported: it is only run as an oracle, as an external program.

## How it will be validated

- Method of manufactured solutions: observed convergence order within 0.1 of theory, h^(p+1) in L2 and h^p in H1 for Pp elements.
- Relative L2 error against the exact solution and the relative residual of the linear solve.
- A solution is never compared with an oracle's mesh node by node; the oracle runs on the same mesh.

## Depends on

go-geometry for meshes, and go-sparse for the linear solvers (its iterative solvers are released; direct solvers are planned for wave 3).

## Scope notes

The plan treats this as an extra-large item, and the MATLAB PDE Toolbox surface is far larger than the Poisson-first plan covers. 3D meshing, Stokes and general elasticity are multi-year.

## Where the plan lives

[PLAN.md](https://github.com/go-scikit/roadmap/blob/main/PLAN.md), [STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md) and the [bibliography](https://github.com/go-scikit/roadmap/blob/main/bib/geometry-pde-graphs.md) in the go-scikit roadmap.
