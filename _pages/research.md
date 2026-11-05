---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<style>
/* Default figure size */
.research-figure {
    max-width: 520px;
    margin: 1.5em auto 2em;
    text-align: center;
}

.research-figure figcaption {
    text-align: center !important;
    margin-top: 0.6rem;
    font-size: 0.9em;
    line-height: 1.5;
}

/* Larger CℓAIR summary figure */
.research-figure.clair-figure {
    max-width: 100%;
}
.research-figure img { display: block; width: 100%; height: auto; border: 1px solid #e6e6e6; border-radius: 4px; }
.research-figure figcaption { margin-top: 0.5em; font-size: 0.82em; line-height: 1.4; color: #626262; }
/* Equal-height appearance without cropping either image or its colorbars. */
.research-figure-pair {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.8rem;
  align-items: center;
}
.research-figure-pair img {
  display: block;
  height: auto;
  border: 0;
  border-radius: 0;
  margin: 0 auto;
  cursor: default;
}
/* The temperature image is narrower in aspect ratio; displaying it at
   83.5% column width balances its HEIGHT with the 3D convection image. */
.research-figure-pair .temperature-image { width: 83.5%; }
.research-figure-pair .convection-image { width: 100%; }
@media (max-width: 600px) {
  .research-figure-pair { grid-template-columns: 1fr; }
}
</style>

## Fully Implicit Runge–Kutta Methods for Time-Dependent PDEs

Fully implicit Runge–Kutta (FIRK) methods offer high-order temporal accuracy and favorable stability properties, but their coupled stages lead to large nonlinear systems. This research develops multigrid and block preconditioners that make these methods practical for time-dependent flow problems.

Recent work focuses on Rayleigh–Bénard convection governed by the incompressible Boussinesq equations. It combines Radau IIA methods with mixed finite element discretizations and investigates two solver strategies: augmented Lagrangian block preconditioning and monolithic multigrid with Vanka relaxation. Numerical experiments examine solver performance in two and three dimensions, including stage dependence and parallel scalability.

**Recent preprint:** [*Scalable Fully Implicit Runge–Kutta Solvers for Time-Dependent Rayleigh–Bénard Convection*](https://arxiv.org/abs/2611.03361) (2026; submitted for publication).

<figure class="research-figure" style="max-width: 100%;">
  <div class="research-figure-pair">
    <img class="temperature-image"
         src="{{ '/images/research/3d_temp.png' | relative_url }}"
         alt="Temperature contours in three-dimensional Rayleigh–Bénard convection"
         loading="lazy">
    <img class="convection-image"
         src="{{ '/images/research/3d_velocity_temp.png' | relative_url }}"
         alt="Three-dimensional velocity streamlines and pressure contours"
         loading="lazy">
  </div>
  <figcaption>Three-dimensional Rayleigh–Bénard convection with Taylor–Hood finite elements and fully implicit Runge–Kutta time integration. Left: temperature field. Right: velocity streamlines and pressure contours.</figcaption>
</figure>

## Algebraic Multigrid for Nonsymmetric and Indefinite Problems

### Optimal Transfer Operators and Convergence Theory

For nonsymmetric linear systems, the choice of restriction and interpolation strongly affects multigrid convergence. This line of work studies optimal two-level methods, sharp convergence bounds, and the role of left and right spectral information in constructing coarse spaces. The aim is to connect rigorous convergence theory with algorithms that remain effective beyond the symmetric positive definite setting.

**Related research:** [*Optimal Transfer Operators in Algebraic Two-Level Methods for Nonsymmetric and Indefinite Problems*](https://doi.org/10.1137/25M179436X), *SIAM Journal on Matrix Analysis and Applications* (2026), and [Generalized optimal AMG convergence theory](https://doi.org/10.1137/24M1679288), *SIAM Journal on Scientific Computing* (2025).

<figure class="research-figure">
  <img src="{{ '/images/research/optimal_amg_theory.png' | relative_url }}" alt="Flow diagram linking left and right eigenvectors to optimal restriction and interpolation in a two-grid method" loading="lazy">
  <figcaption>Relationship between spectral information and optimal two-grid transfer operators.</figcaption>
</figure>

### Reduction-Based Algebraic Multigrid

The constrained local approximate ideal restriction (CℓAIR) approach develops local approximations to ideal restriction while enforcing constraints associated with important error modes. This provides an algebraic multigrid strategy for problems in which nonsymmetry and strong advection make conventional approaches challenging.

**Related research:** [CℓAIR, *SIAM Journal on Scientific Computing* (2024)](https://doi.org/10.1137/23M1583442).

<figure class="research-figure clair-figure">
  <img src="{{ '/images/research/clair_website_summary.png' | relative_url }}" alt="Comparison of multigrid iteration counts and work per digit as problem size increases" loading="lazy">
  <figcaption>
  CℓAIR: Robust algebraic multigrid across advection–diffusion
  regimes. Left: Solver convergence as the diffusion parameter
  varies. Right: Operator complexity for representative
  diffusion problems.
</figcaption>
</figure>

## Scalable Solvers for Kinetic Plasma Models

Earlier collaborative work with Los Alamos National Laboratory applied reduction-based multigrid to systems arising from a relativistic drift-kinetic Fokker–Planck–Boltzmann model of runaway electrons. The computational challenge is to solve large, nonsymmetric systems efficiently within an implicit nonlinear simulation. This research connects ℓAIR multigrid to demanding applications in plasma physics.

<figure class="research-figure">
  <img src="{{ '/images/research/runaway_electrons.png' | relative_url }}" alt="Numerical distribution produced by a runaway-electron model" loading="lazy">
  <figcaption>Runaway distribution in a Relativistic Fokker–Planck-Boltzmann model.</figcaption>
</figure>

## Current Research Group — Cross Scholar Projects

Both student research projects are conducted through the Cross Scholar program.

### Wave Propagation in Heterogeneous Excitable Media

**Student researchers:** Abdul Ahad and Dikshant Aryal  
**Project:** *Wave Propagation in Heterogeneous Excitable Media: Numerical Simulation and Machine Learning with the FitzHugh–Nagumo Model*

This ongoing project examines how spatial heterogeneity affects excitation and wave propagation in the FitzHugh–Nagumo reaction–diffusion system. The work brings together mathematical modeling, numerical simulation, and machine-learning approaches.

### Low-Rank Compression of Transformer Weights

**Student researcher:** Sujjal Chapagain  
**Project:** *Numerical Linear Algebra Techniques for Low-Rank Compression of Transformer Weights*

This ongoing project explores low-rank matrix approximation techniques for reducing the storage and computational costs of transformer models, with attention to the trade-off between compression and approximation accuracy.
