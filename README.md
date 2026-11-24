# A Natural-Language Proof of the Riemann Hypothesis

English · [简体中文](README.zh-CN.md)

This project presents a [self-contained natural-language proof of the Riemann hypothesis (PDF)](main.pdf), written with help from GPT and based on [Levent Alpöge’s Lean proof](https://github.com/leanprover-community/riemann-hypothesis/blob/a172c464fd4bcfc4f53e394dcba45d742b1409a6/src/Main.lean#L4). This is an independently maintained personal project and does not represent Alpöge or any organization.

---

[Chapter 1, *Introduction* (pp. 19–44)](main.pdf#page=19) gives an overview of the argument.

- Start with a hypothetical zero $\rho$ to the right of the critical line and inside the critical strip. After subtracting the known contribution at $s=1$ from a smoothed sum over prime powers, its Mellin transform still has a pole at $\rho$. [§§1.1–1.2](main.pdf#page=20)
- Combine the sums for a family of Dirichlet characters into a real sum $G(x)$. Its positive weights keep the zero multiplicities from cancelling, so the pole survives. The arithmetic goal is a one-sided upper bound on $G(x)$. [§1.3](main.pdf#page=23)
- Recover $G(x)$ from a chain of theta lifts. A finite Fourier average selects the desired character contributions from the local arithmetic data, leaving an error to estimate. [§1.4](main.pdf#page=25)
- Bound that error on the same chain. Period pairings connect the complex integrals to integral lattices. Geometry controls the lattice indices, while interpolation and Gram matrix estimates control how many independent directions survive. [§§1.5–1.8](main.pdf#page=31)
- Choose the chain length $m$ near $\sqrt{x}$ to balance errors of sizes $x/m$ and $m$. This gives $G(x)\le x^{1/2+9\varepsilon}$ throughout $[Y,Y^{3/2}]$ for arbitrarily large $Y$ and sufficiently small $\varepsilon \gt 0$. [§1.9](main.pdf#page=40)
- Return to the zero. Choose $1/2+9\varepsilon \lt \operatorname{Re}(\rho)$. The interval bound controls a pair of high derivatives of the Laplace transform, while a nearby pole forces incompatible growth. This rules out zeros on the right of the critical line in the strip. The functional equation then rules them out on the left. [§§1.10–1.11](main.pdf#page=41)

---

The Riemann hypothesis has been proved, and the work of understanding the theorem has only just begun. Questions about the natural-language proof or the original Lean files are welcome in this repository’s Issues, as are corrections and suggestions for improving the exposition. The maintainer will reply regularly with help from GPT, in the hope that everyone can learn something.
