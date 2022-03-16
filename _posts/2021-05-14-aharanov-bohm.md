---
title: "The Aharanov-Bohm Effect"
date: 2021-05-14
permalink: /posts/2021/05/14/blog-post/
categories:
  - blog
tags:
  - physics
  - lesson
---

What is the vector potential, really? Besides a mathematical trick envoked to exploit the fact that the magnetic is always incompressible, undergraduates (such as myself) were never shown a satisfying explanation. We go through our electromagnetism classes spiting it, thinking to ourselves that "if the universe were more symmetric, it wouldn't exist!" when in fact the truth could not be more different. This strange potential function is undoubtedly the most used and applied field in all of physics, and its importance to the theory of quantum mechanics, from lattice gauge theory to particle physics, cannot be overstated. In what follows, I hope to convince you, a young physicist of limited knowledge and strong conviction, that this potential is not simply a mathematical construct. That it is perhaps the piece with the deepest and most resonant consequences.

We begin, as we should, with the fact that $\nabla \cdot \mathbf{B} = 0$. We can thus always express our system's magnetic behaviour via a so-called vector potential $\mathbf{A}$. This has a few important upsides, none of which will be discussed here. Now we are all too happy to work with this potential and simply take its curl to recover the magnetic field, but we might also take a step back and notice something. 

Greater, more universal physics cannot be derived from the laws which we understand now. If this were the case, those current laws *are* the more universal ones, and hence need not be derived. Entropy was stumbled upon while studying heat engines. Planck's constant was a trick to make integrals converge. The vector potential was a mathematical convenience with no real physical significance.

Here's where things get interesting. To understand what we're about to do, we need 3 key pieces:

1. The vector potential of a solenoid;
2. The effect of magnetism on the energy;
3. The phase picked up travelling along a path.

The first is the easiest. Ampère's law says that the magnetic field inside a solenoid is constant and pointing along the axis, while outside it is 0. The vector potential outside the solenoid must therefore be 

$$\mathbf{A}=\left(\frac{B_0 R^2}{2r}\right)$$

satisfying $\nabla \times \mathbf{A} = 0$. 

The second is slightly more involved. Here's the gist: upon applying a magnetic field, your momentum is shifted. This is called the *minimal substitution*, and it's due to the pesky $q \mathbf{A} \cdot \mathbf{v} /c$ term that pops up in the Lagrangian to satisfy the Lorentz force equation. At the end of the day, turning on a magnetic field will take $L \rightarrow L+q \mathbf{A} \cdot \mathbf{v} /c$ and $\mathbf{p} \rightarrow \mathbf{p} - q\mathbf{A}/c$.

The third is the hardest to justify heuristically, so I'll just spit it out: the quantum probability amplitude to take a given path is proportional to 

$$e^{i\frac{S(x,t)}{\hbar}}$$

where $S(x,t) = \int_{t_0}^t dt' L(x,t')$, and $L$ is the usual Lagrangian from classical mechanics.

Now, let's consider an experiment with two slits, and let's put a solenoid on our side in between those slits. A classical physicist, and even you perhaps, might expect that since there is no magnetic field, there should be no difference between the two particles. After all, fields are what make physics! Potentials are strictly convenience. I hope you see how that will change. Even if you don't, follow along.

There are two paths equally classical paths the particle can take to get from the source to a point on the screen, call them paths 1 and 2. The amplitudes are each modified:

$$\psi_1 \rightarrow \psi_1 \exp \left[i \left(\frac{q}{\hbar c}\right) \int_{\text{path 1}} \mathbf{A}\cdot \mathbf{dr} \right] \\
\psi_2 \rightarrow \psi_2 \exp \left[i \left(\frac{q}{\hbar c}\right) \int_{\text{path 2}} \mathbf{A}\cdot \mathbf{dr} \right]$$.

Here, we've used the fact that $\mathbf{v} dt = \mathbf{dr}$. To get the total amplitude, add these up, extract out a global phase, and bring the line integrals into surface integrals via Stokes' theorem. Stokes' is extra neat here, since 

$\int \mathbf{A} \cdot \mathbf{dr} = \int \nabla \times \mathbf{A} \cdot \mathbf{dS}= \int \mathbf{B}\cdot \mathbf{dS}$.

All in all, the probability amplitude to end up at a point on the screen is

$\psi_1\exp \left[i \left(\frac{q}{\hbar c}\right) \oint \mathbf{B}\cdot \mathbf{dS} \right]+\psi_2$
which is not the same as without the magnetic field! Indeed, the integral is simple if the magnetic field is constant: it is $\pi R^2 B_0$. And the factors in front are just the flux quanta $\phi_0$. So we have a ratio of fluxes

$\Phi = \frac{B_0 \pi R^2}{\phi_0}$.

When this quantity is a factor of $2\pi$, everything is the same as before. But, in the case where $\Phi = (2n+1)\pi$, the position of the the diffraction minima and maxima are interchanged! Not bad for a mathematical construct with no standalone physical consequence. Even if the magnetic field is null everywhere the particles travel, the vector potential is not, leading to very real physical consequences i.e. an interference pattern.

I hope I've convinced you that when it comes to introductory electromangetism, not is all that meets the eye. It is important to be aware of the role of the vector potential in quantum mechanics, since it pops up everywhere! Spoiler alert: it's a quantum harmonic oscillator.

