---
permalink: /
title: "Welcome!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>

/* True watermark on homepage */
body::before {
  content: "";
  position: fixed;
  top: 80px;
  left: 0;
  width: 100%;
  height: calc(100% - 80px);

  background-image: url("/assets/images/usm-watermark.png");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 850px auto;

  opacity: 0.15;

  pointer-events: none;
  z-index: 0;
}

/* Keep actual webpage content above watermark */
#main,
.masthead,
.page__footer {
  position: relative;
  z-index: 1;
}

/* Slight white veil behind main article for readability */
.page {
  background: rgba(255, 255, 255, 0.88);
  padding: 1.2rem 1.5rem;
  border-radius: 10px;
}

/* Homepage paragraph formatting */
.page__content p {
  text-align: justify !important;
  line-height: 1.65;
}

</style>

I am Ahsan Ali, a Tenure-track Assistant Professor of Applied and Computational Mathematics in the School of Mathematics and Natural Sciences at [The University of Southern Mississippi (USM)](https://www.usm.edu/). My research lies at the intersection of numerical analysis, scientific computing, and partial differential equations, with a particular emphasis on scalable numerical solvers and multilevel methods for nonsymmetric and indefinite problems. I develop and analyze algebraic multigrid (AMG) methods, scalable preconditioners, and time-integration algorithms for challenging PDE systems arising in computational science and engineering.

Before joining USM, I was a Postdoctoral Research Associate at [Baylor University](https://www.baylor.edu/), where I worked on an NSF-funded project focused on the [Irksome library](https://www.firedrakeproject.org/Irksome/), a high-level software package for time-stepping finite element discretizations of partial differential equations. My work involved developing and extending numerical algorithms and software for implicit time integration and scalable solution techniques for complex PDE problems.

I hold a B.Sc. in Mathematics (2011) and an M.S. in Mathematics (2012) from [Jahangirnagar University](https://juniv.edu/), Dhaka, Bangladesh. I later earned an M.S. in Applied Mathematics (2024) and a Ph.D. in Applied Mathematics (2025) from the [University of New Mexico (UNM)](https://www.unm.edu/). My dissertation, *Algebraic Multigrid Methods for Nonsymmetric and Indefinite Problems: Theory and Applications*, focused on the development and analysis of robust multilevel methods for challenging linear systems arising from partial differential equations.

My research includes interdisciplinary collaborations with national laboratories and academic institutions, with interests spanning algebraic multigrid, finite element methods, high-performance scientific computing, implicit Runge–Kutta methods, computational fluid dynamics, and kinetic plasma models.

With over seven years of formal teaching experience and more than a decade of involvement in mathematics education, I have designed and taught courses ranging from undergraduate calculus to numerical analysis. I enjoy connecting mathematical theory with computational applications and involving students in research-oriented mathematical and scientific computing problems.

When I am not working on mathematics or mentoring students, I enjoy traveling, spending time with my daughter, and following the latest developments in technology.