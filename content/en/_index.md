---
title: "go-fem documentation"
linkTitle: "Home"
type: docs
cascade:
  type: docs
description: "go-fem (planned, wave 3): finite elements and PDE solvers in pure Go (CGO=0): Lagrange P1/P2 elements, quadrature, assembly and boundary conditions, Poisson, heat and elasticity, validated by manufactured solutions."
---

**go-fem is planned, in wave 3.** It holds no library yet: no repository
contains code, and nothing here is released. These pages say what the
organization will cover, which items of the plan it carries, and which
references each package will be validated against.

## Scope

Finite elements and PDE solvers.

## The plan

In the [go-scikit roadmap](https://github.com/go-scikit/roadmap),
[PLAN.md](https://github.com/go-scikit/roadmap/blob/main/PLAN.md) puts this
organization at item 13 of wave 3 (go-geometry meshing and go-fem: P1/P2 elements, Poisson, heat, elasticity, validated by manufactured solutions). The plan's rules apply to every item: pure Go (CGO=0) on
every architecture the fleet's CI tests, a bibliography read before any code,
validation against the tools that are the reference in the domain (run as
oracles, never ported when their licence forbids it), unit and regression tests
at 100% coverage, and a performance table against the reference tool.

## Status

[STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md) lists
each item of the plan with its repository, pull requests, release and measured
parity. This organization's items are **planned**. The evidence behind the scope
(function inventories, algorithms, reference implementations and licences,
validation oracles) is in the roadmap's
[bibliography](https://github.com/go-scikit/roadmap/blob/main/bib/geometry-pde-graphs.md).

## The planned packages

The package names are working names. None exists as a repository yet.

| Package | Status | What it will provide |
| --- | --- | --- |
| [fem]({{< relref "fem" >}}) | planned (wave 3), no repository yet | Lagrange finite elements, quadrature, assembly, boundary conditions and the first PDE solvers. |
| [mms]({{< relref "mms" >}}) | planned (wave 3), no repository yet | The shared method-of-manufactured-solutions convergence harness. |

## Licences

MFEM (BSD-3-Clause) is the clean design reference and deal.II's Apache-2.0 side permits a port after each file's SPDX header is checked. FEniCS and DOLFINx are LGPL-3.0 and are oracles only.

## Neighbouring organizations

go-geometry provides the meshes, go-sparse the linear solvers and go-numerics the stiff time integrators the heat and wave equations need.

## What each package's pages hold

| Package | Pages |
| --- | --- |
| fem | [overview]({{< relref "fem" >}}) |
| mms | [overview]({{< relref "mms" >}}) |
