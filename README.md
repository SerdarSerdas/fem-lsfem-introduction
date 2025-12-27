# Introduction

The finite element method (FEM) is a cornerstone numerical technique for the approximate solution of partial differential equations (PDEs) that arise in modeling a broad range of physical phenomena, including **fluid flow, heat transfer, porous media transport, and fluid-structure interaction**.

## Classical Galerkin FEM

The classical Galerkin finite element method discretizes the weak (variational) form of PDEs by projecting onto finite-dimensional approximation spaces, typically constructed from piecewise polynomial basis functions. Despite its widespread use and theoretical foundation, the Galerkin method can experience numerical instabilities, especially in **convection-dominated transport problems** and **saddle-point systems** such as the incompressible Navier-Stokes equations. These instabilities often lead to spurious oscillations and may violate the **Ladyzhenskaya-Babuška-Brezzi (LBB)** condition necessary for stable velocity-pressure coupling in mixed formulations.

## Least-Squares FEM (LSFEM)

**LSFEM** addresses these limitations by recasting the PDE system into a minimization problem that seeks the approximate solution $u_h \in V_h$ minimizing the least-squares functional:

$${\cal F}(u_h) = \parallel {\cal L} u_h - f \parallel^2_0$$

where ${\cal L}$ is the differential operator, $f$ is the forcing term, and $\parallel \bullet \parallel^2_0$ denotes the **$L_2$-norm**.

This reformulation **guarantees a symmetric positive-definite system matrix**, yielding improved stability characteristics and permitting the use of **equal-order finite element spaces** for all variables without additional stabilization or mixed element constraints. Furthermore, by minimizing the residual globally, LSFEM inherently provides stabilization for advection-dominated regimes, ensuring convergence and suppressing non-physical oscillations.

## Systematic Comparison

This study presents a **systematic comparison** between standard Galerkin FEM and **adaptive LSFEM** applied to:

- **Poisson equation**
- **Advection-diffusion-reaction equation** 
- **Stokes and incompressible Navier-Stokes equations**
- **Multiphase flow** (Theory of Porous Media)
- **Fluid-structure interaction (FSI)**

**Adaptive mesh refinement** guided by **LSFEM residual error indicators** enhances accuracy in regions with steep gradients.

## Performance Evaluation

Focus: **numerical stability, convergence rates, error norms, computational cost**.
