# Academic Mathematics Projects — IIT Kanpur

A collection of three academic projects completed as part of the Master of Science (M.Sc.) in Mathematics curriculum at the **Department of Mathematics and Statistics, Indian Institute of Technology Kanpur (IIT Kanpur)**. These projects span computational nonlinear dynamics, operator theory & numerical functional analysis, and category theory.

---

## Overview

| https://www.google.com/search?q=%23 | Project | Course | Instructor | Core Focus | Artifacts |
|:-:|:--------|:-------|:-----------|:-----------|:----------|
| 1 | [Chaos and Bifurcation Analysis in the Gray-Scott Model](#) *(PDF)* | **MTH658A** | Prof. Malay Banerjee | Reaction-diffusion PDEs, linear stability, bifurcation analysis, Lyapunov exponents | `Chaos and Bifurcation Analysis.pdf`, MATLAB scripts (`Simu.m`, `lyaa.m`) |
| 2 | [Approximation of Spectra of Linear Operators on Hilbert Space](#) *(PDF)* | **MTH616A** *(Theoretical Numerical Mathematics)* | Prof. Akash Anand | Finite-section method, quasidiagonality, Hausdorff spectral convergence | `linear operators on Hilbert space.pdf` |
| 3 | [Special Adjoint Functor](#) *(PDF)* | **MTH202A** *(Set Theory and Discrete Mathematics)* | Prof. Amit Shekhar Kuber | Special Adjoint Functor Theorem (SAFT), Stone-Čech compactification, filtered colimits | `Special Adjoint Functor.pdf` |

*(Update the links in the table above to point to the relative file paths in your GitHub repository once uploaded.)*

---

## 1. Chaos and Bifurcation Analysis in the Gray-Scott Model: A Computational Exploration

- **Course:** MTH658A | **Instructor:** Prof. Malay Banerjee | **Date:** November 12, 2023
- **Report:** `Chaos and Bifurcation Analysis.pdf`

### Summary
This project computationally investigates spatio-temporal pattern formation, bifurcations, and chaotic behavior in the **Gray-Scott reaction-diffusion system**, which models the interaction of two chemical species—an activator ($U$) and an inhibitor ($V$):

$$\frac{\partial U}{\partial t} = D_u \nabla^2 U - U V^2 + F(1 - U)$$

$$\frac{\partial V}{\partial t} = D_v \nabla^2 V + U V^2 - (F + k)V$$

where $D_u, D_v$ are diffusion rates, $F$ is the feed rate, and $k$ is the kill rate.

### Key Highlights
- **Analytical Stability & Bifurcations:** Derives steady-state critical points $(U_c, V_c)$ and linearizes the PDE system ($\partial_t \mathbf{X} = \mathbf{J}\mathbf{X}$) to characterize stability via eigenvalues and identify pitchfork, saddle-node, and Hopf bifurcations.
- **2D Pattern Formation Simulation (`Simu.m`):** Numerically integrates the 2D Gray-Scott equations on a $200 \times 200$ grid ($D_u = 0.16$, $D_v = 0.08$, $F = 0.035$, $k = 0.06$, $\Delta t = 1$, $T = 10000$) using discrete Laplacian operators (`del2`), capturing the evolution from localized perturbations ($t = 100, 700$) to intricate self-organized spots and labyrinthine stripe structures ($t = 3400, 10000$).
- **Bifurcation Sweep & Lyapunov Exponents (`lyaa.m`):** Varies the feed rate $F \in [0.03, 0.06]$ (with $k = 0.065$, $N_x = 100$, $T = 5000$) and computes finite-difference Lyapunov exponents via perturbation renormalization to quantify sensitivity to initial conditions.

### Tools & References
- **Tools:** MATLAB, LaTeX
- **References:** Alligood et al. (1998); Strogatz (1996); Wang & Jia (2019).

---

## 2. Approximation of Spectra of Linear Operators on Hilbert Space

- **Course:** MTH616A — Theoretical Numerical Mathematics | **Instructor:** Prof. Akash Anand
- **Report:** `linear operators on Hilbert space.pdf`

### Summary
This project studies the mathematical theory behind approximating the spectrum $\sigma(A)$ of continuous (and not necessarily bounded) linear operators acting on an infinite-dimensional, complex, separable Hilbert space $\mathcal{H}$, addressing why finite-dimensional matrix convergence intuitions break down in infinite dimensions.

### Key Highlights
- **Finite-Section Method & Compressions:** Examines finite-rank orthogonal projections $P_n \to I$ strongly and operator compressions $A_n = P_n A|_{P_n \mathcal{H}}$ to analyze how $\sigma(A_n)$ evolves as $n \to \infty$.
- **Essential vs. Transient Spectrum & Operator Degree:** Introduces filtrations $\mathcal{F} = \{\mathcal{H}_n\}$ of finite-dimensional subspaces and the operator degree $\deg(A) = \sup_{n \geq 1} \operatorname{rank}(P_n A - A P_n)$ (abstracting band-limited infinite matrices) to establish when the essential spectrum satisfies $\sigma_e(A) = \Lambda_e$.
- **Quasidiagonality & Decomposition:** Covers quasidiagonal and block-diagonal operators, including the Weyl–von Neumann–type decomposition $A = D + C$ (diagonal plus compact perturbation) for normal and self-adjoint operators.
- **Hausdorff Spectral Convergence:** Presents the convergence theorem showing that for a self-adjoint operator $A$ quasi-diagonalized by $\{P_n\}$ and any compact set $K \subset \mathbb{R}$, $\sigma(P_n A|_{P_n \mathcal{H}}) \cap K \to \sigma(A) \cap K$ in the Hausdorff distance as $n \to \infty$.

### References
- Arveson (1991); Hansen (2008); Kato (1949, 2013); Pokrzywa (1981).

---

## 3. Special Adjoint Functor

- **Course:** MTH202A — Set Theory and Discrete Mathematics | **Instructor:** Prof. Amit Shekhar Kuber
- **Report:** `Special Adjoint Functor.pdf`

### Summary
This project provides a rigorous exposition of the **Special Adjoint Functor Theorem (SAFT)** in category theory, its application to topology, and the structure of **filtered categories** and **filtered colimits**.

### Key Highlights
- **Special Adjoint Functor Theorem (SAFT):** States and proves (following Mac Lane) that for locally small categories $\mathcal{C}, \mathcal{D}$ where $\mathcal{D}$ is complete, well-powered, and possesses a coseparating set of objects, a functor $G: \mathcal{D} \to \mathcal{C}$ has a left adjoint if and only if $G$ preserves small limits—established via an initial-object construction using products, equalizers, and pullbacks.
- **Application — Stone-Čech Compactification:** Applies SAFT to prove that the inclusion functor $I: \mathbf{KHaus} \to \mathbf{Top}$ from Compact Hausdorff Spaces to Topological Spaces admits a left adjoint $F$ (the canonical Stone-Čech compactification), verifying completeness via Tychonoff's theorem, well-poweredness via closed subspaces, and the singleton coseparator $\{[0, 1]\}$.
- **Filtered Categories & Colimits:** Defines filtered categories and directed sets, proves that a category is co-complete iff it is co-cartesian and has all small filtered colimits, and highlights the commutation of filtered colimits with finite limits in $\mathbf{Sets}$ and algebraic categories ($\mathbf{Alg}$).

### References
- Cunha (2013); Lawvere (1966); Mac Lane (2013); Nguyen, Raptis & Schrade (2020).

---

## Repository Structure

```text
.
├── Chaos and Bifurcation Analysis.pdf
├── linear operators on Hilbert space.pdf
├── Special Adjoint Functor.pdf
└── README.md
```

---

## Author

**Abhishek Pandey**  
M.Sc. Mathematics (Roll No. 221253)  
Department of Mathematics and Statistics, IIT Kanpur
