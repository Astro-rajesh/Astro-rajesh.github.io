---
layout: single
title: "Listening to the Hidden Magnetic Fields of the Sun"
permalink: /research/forced-dynamo-fmode/
author_profile: true
math: true
---

> *Can we detect magnetic fields beneath the solar surface without seeing them directly?*

---

## The Mystery

The Sun constantly oscillates. These oscillations carry information about the solar interior, allowing us to probe regions that cannot be observed directly. Much like seismic waves reveal Earth's interior, solar oscillations provide a window into the hidden layers beneath the photosphere.

Yet one of the greatest challenges in solar physics remains understanding the magnetic field below the solar surface.

Can waves reveal what telescopes cannot?

> **Figure:** Solar image or illustration of helioseismic waves.

---

## Why the $f$-mode?

The Sun supports many kinds of oscillations, but the $f$-mode is special because it is confined to the solar surface. Its amplitude is largest at the photosphere and decays exponentially away from it, making it highly sensitive to conditions just beneath the surface. This makes the $f$-mode an ideal probe of subsurface magnetic fields.

> **Figure:** Illustration comparing $p$-modes and the $f$-mode.
> 
If you're not familiar with surface gravity waves, this short introduction from the University of Waterloo provides a good starting point: [Surface Gravity Waves](https://uwaterloo.ca/applied-mathematics/current-undergraduates/continuum-and-fluid-mechanics-students/amath-463/surface-gravity-waves)

---

## The Scientific Question

> **Can magnetic fields beneath the solar surface leave measurable signatures on the f-mode?**

This question motivated the project.

---

## Building the Numerical Experiment

Instead of simulating the entire Sun, we build an idealized numerical model that captures the physics most relevant to surface gravity waves. As shown in Figure 1, the computational domain consists of two isothermal layers separated by an interface at $z=0$, representing the solar surface. The $f$-mode is confined to this interface, where its amplitude is largest and decreases exponentially away from it. This makes the wave an excellent probe of magnetic fields located just beneath the surface.

<figure class="align-center">
  <img src="/assets/images/research/rho_pre_tem.png"
       alt="Computational domain"
       style="width:70%; max-width:700px;">
  <figcaption>
    <strong>Figure 1.</strong> Computational domain.
  </figcaption>
</figure>

---

## Generating the Magnetic Field

Previous studies have shown that subsurface magnetic fields can leave clear signatures on the $f$-mode. However, these studies typically considered either idealized analytical magnetic structures or magnetic fields imposed by hand in numerical simulations. An important open question is whether these signatures survive when the magnetic field is generated self-consistently by a turbulent dynamo.

To answer this, we use a helically forced $\alpha^2$ dynamo operating in the lower layer of our computational domain. Turbulence is continuously driven by a helical forcing function, which amplifies a weak seed magnetic field through dynamo action. As the magnetic energy grows, it eventually reaches a statistically steady (**saturated**) state, where the magnetic field is maintained by the ongoing turbulent motions. It is this self-generated magnetic field that interacts with the surface gravity waves in our simulations.

<figure class="align-center">
  <img src="/assets/images/research/b_rms-t.png"
       alt="Computational domain"
       style="width:70%; max-width:700px;">
  <figcaption>
    <strong>Figure 2.</strong> Time evolution of the kinetic and magnetic energies.
  </figcaption>
</figure>

---

## Listening to the Waves

Once the magnetic field reaches its saturated state, we begin "listening" to the waves propagating through the simulation. We record the vertical velocity at the surface over time, capturing the oscillations excited by the turbulent motions.

To identify the different wave modes, we perform a two-dimensional Fourier transform in space and time. This produces a **$k$–$\omega$ diagram**, where each ridge corresponds to a different type of wave. The surface gravity ($f$) mode appears as a distinct ridge, clearly separated from the acoustic ($p$) modes.

By comparing the $f$-mode in the hydrodynamic and dynamo simulations, we can measure how the self-generated magnetic field modifies its properties.

<figure class="align-center">
  <img src="/assets/images/research/kom.png"
       alt="k–ω diagram showing the f-mode and p-modes"
       style="width:100%; max-width:900px;">
  <figcaption>
    <strong>Figure 3.</strong> The $k$–$\omega$ diagram obtained from the simulated surface oscillations. The left panel shows the power spectrum in the hydrodynamic case, while the right panels compare the mode profiles before and after the magnetic field reaches its saturated state. The shift of the $f$-mode ridge provides a direct measure of the influence of the dynamo-generated magnetic field.
  </figcaption>
</figure>

---

## What We Found

The answer is **yes**.

During the early (**kinematic**) phase of the dynamo, the magnetic field is too weak to influence the flow. As a result, the *f*-mode is almost indistinguishable from that of a nonmagnetic simulation. In other words, the presence of a weak, growing magnetic field alone does not affect the surface waves.

The picture changes once the dynamo reaches its **saturated** state. The self-generated large-scale magnetic field begins to interact with the flow, leaving clear signatures on the $f$-mode. We find that the magnetic field:

- **increases the frequency** of the $f$-mode,
- **strengthens** the mode, making it more prominent in the power spectrum, and
- **broadens** the mode, producing the characteristic fanning-out seen in the $k$–$\omega$ diagram.

These effects become stronger as the magnetic field near the surface increases, suggesting that the *f*-mode carries valuable information about subsurface magnetism.

<figure class="align-center">
  <img src="/assets/images/research/modes_char_com.png"
       alt="Computational domain"
       style="width:70%; max-width:700px;">
  <figcaption>
    <strong>Figure 4.</strong> Comparison of the $f$-mode in the kinematic and saturated phases, highlighting the frequency shift and enhanced mode strength.
  </figcaption>
</figure>

---

## Why It Matters

Our simulations show that the signatures of subsurface magnetic fields on the $f$-mode are not an artifact of imposing magnetic fields by hand. They persist even when the magnetic field is generated self-consistently through dynamo action. This strengthens the idea that the $f$-mode can be used as a reliable probe of hidden solar magnetism.

Although our model is highly idealized and is **not** intended to represent the solar dynamo in all its complexity, it captures an essential piece of the physics: the interaction between surface gravity waves and dynamically generated magnetic fields. By isolating this interaction, we can better understand how magnetic fields influence helioseismic observations.

Ultimately, our goal is to move toward more realistic models with convective turbulence and solar-like stratification. If the same signatures persist under those conditions, the $f$-mode could become a valuable diagnostic tool for detecting magnetic fields beneath the solar surface and, potentially, for identifying active regions before they emerge.

---

## Publication

**Rajesh Mondal & N. K. Singh (2026)**

*Effects of Dynamo-Generated Large-Scale Magnetic Fields on the Surface Gravity (f) Mode*

The Astrophysical Journal Letters **1004**, L38

[DOI](https://doi.org/10.3847/2041-8213/ae6fbb) |
[PDF](https://iopscience.iop.org/article/10.3847/2041-8213/ae6fbb/pdf) |
[arXiv](https://arxiv.org/abs/2602.05529)

---

## What's Next?

**Coming soon:** More realistic solar models, convective dynamos, and the next chapter of this research.
