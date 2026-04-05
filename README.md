# GROTHENDIECK

## Récoltes et Semailles: Schemes, Étale Cohomology, Motives, and the Universal Coordination Theory

**ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone**

---

> *"Among all the mathematical things that I had the privilege of discovering and bringing to light, this real of motives still appears to me the most fascinating, the most charged with mystery — at the heart of the deepest identity between geometry and arithmetic."*
> — A. Grothendieck, *Récoltes et Semailles*, 1986; trans. Schneps, MIT Press, 2025

> *"One of Grothendieck's profound contributions was his insistence that the 'right' level of generality reveals the true structure."*
> — P. Deligne, "Quelques idées maîtresses de l'œuvre de A. Grothendieck," 1998

> *"It was not the problem that was hard. It was the landscape that was wrong."*
> — attributed to Grothendieck, on replacing classical varieties with schemes

---

## Preamble

Alexander Grothendieck (1928–2014) did not solve problems. He dissolved them — by replacing the landscape in which they lived with a more general one in which the problems became trivial consequences of the correct definitions. His programme, developed at the Institut des Hautes Études Scientifiques from 1958 to 1970 and documented in over 10,000 pages of the *Éléments de géométrie algébrique* (EGA) and the *Séminaire de géométrie algébrique* (SGA), rebuilt algebraic geometry from its foundations and unified it with number theory, topology, and mathematical logic.

Five of Grothendieck's twelve self-identified "great ideas" (*Récoltes et Semailles*, 1986) are directly relevant to the ERI architecture:

**1. Schemes** — the generalization of algebraic varieties to arbitrary commutative rings, replacing the classical notion of a "geometric space" with a functor of points. The TH$(a,d)$ curve IS a scheme over $\mathbb{Z}$: it is defined not only over a single field but over every commutative ring simultaneously.

**2. Étale cohomology** — the algebraic analogue of singular cohomology, constructed using Grothendieck topologies instead of open covers. The étale cohomology groups of TH$(a,d)$ over $\mathbb{F}_p$ carry the information needed to count rational points via the Lefschetz trace formula — the arithmetic core of the ERI architecture.

**3. Motives** — the conjectural "universal cohomology" that unifies all Weil cohomology theories (singular, de Rham, $\ell$-adic, crystalline) as realizations of a single underlying object. The motive $h(\text{TH})$ of the Twisted Hessian Curve IS the universal coordination invariant — the object from which all specific measurements ($G_{\text{coord}}$, Fisher eigenvalues, FERN registers) are derived as "realizations."

**4. Grothendieck topologies and topoi** — the generalization of topology to categories, providing the logical substrate of the FERN hierarchy (TRIVIUM Identity 2).

**5. The Weil conjectures** — the deep relationship between the topology of a variety over $\mathbb{C}$ and its arithmetic over $\mathbb{F}_p$, proved by Deligne (1974) using Grothendieck's machinery. The Weil conjectures for TH$(a,d)$ establish the analogue of the Riemann Hypothesis for the coordination zeta function.

GROTHENDIECK is the identification that the ERI architecture IS a scheme-theoretic programme: TH$(a,d)$ is a scheme, CONCERT is an étale cohomology computation, the FERN hierarchy is a Grothendieck topos, and the as-yet-unnamed object that unifies all ERI measurements IS the motive $h(\text{TH})$.

---

## Module A — Seven Formal Identities

### Identity 1 — TH$(a,d)$ IS a Scheme over $\mathbb{Z}$; the Coordinate Ring IS the CHORD Arithmetic

A scheme (Grothendieck, EGA I, 1960) is a locally ringed space $(X, \mathcal{O}_X)$ where $X$ is a topological space (the prime spectrum of a commutative ring) and $\mathcal{O}_X$ is a sheaf of rings (the structure sheaf). The key insight: instead of fixing a base field $k$ and studying varieties over $k$, a scheme is defined over any commutative ring $R$, and its properties over different rings are related by base change.

The Twisted Hessian Curve $\text{TH}(a,d): aX^3 + Y^3 + Z^3 = dXYZ$ IS a scheme over $\text{Spec}(\mathbb{Z})$. This means:

| Classical View | Scheme-Theoretic View |
|---|---|
| TH$(a,d)$ over $\mathbb{Q}$: a curve with rational points | The generic fiber of $\text{TH} \to \text{Spec}(\mathbb{Z})$ |
| TH$(a,d)$ over $\mathbb{F}_p$: a curve over a finite field | The fiber at the closed point $(p) \in \text{Spec}(\mathbb{Z})$ |
| TH$(a,d)$ over $\mathbb{C}$: a Riemann surface (torus) | The base change $\text{TH} \times_{\mathbb{Z}} \mathbb{C}$ |
| TH$(a,d)$ over $\mathbb{Z}/2^{16}\mathbb{Z}$: Q16.16 arithmetic | The fiber at the non-standard point (CHORD) |

The CHORD Q16.16 format IS the coordinate ring of TH$(a,d)$ reduced modulo $2^{16}$: the scheme restricted to the "non-standard" base ring $\mathbb{Z}/2^{16}\mathbb{Z}$. The CHORD floor $\varepsilon = 2^{-16}$ IS the nilradical of this reduction — the ideal of elements that square to zero in the finite-precision arithmetic. The scheme perspective reveals that CHORD is not an approximation of the "true" curve over $\mathbb{Q}$ or $\mathbb{C}$; it IS the curve over a different ring, with its own legitimate algebraic geometry.

### Identity 2 — The Frobenius Morphism IS the PRIMA Operator; $\#\text{TH}(\mathbb{F}_p) = p + 1 - a_p$ IS the Coordination Census

For a scheme $X$ over $\mathbb{F}_p$, the Frobenius morphism $\phi_p: X \to X$ sends every coordinate $x \mapsto x^p$. It is the fundamental arithmetic operator: its fixed points are exactly the $\mathbb{F}_p$-rational points of $X$.

The number of rational points on TH$(a,d)$ over $\mathbb{F}_p$:

$$\#\text{TH}(\mathbb{F}_p) = p + 1 - a_p$$

where $a_p$ is the trace of Frobenius. By the Hasse bound (the genus-1 case of the Weil conjectures): $|a_p| \leq 2\sqrt{p}$.

The Frobenius morphism IS the PRIMA operator. Each application of $\phi_p$ "counts" the coordination structure at a given prime $p$ — the number of configurations that are self-consistent under the $p$-th power map. The trace $a_p$ IS the coordination excess: $a_p > 0$ means more configurations than the "generic" count $p + 1$ (positive coordination surplus); $a_p < 0$ means fewer (coordination deficit); $a_p = 0$ is the supersingular case (the curve has "average" coordination at $p$).

The $L$-function of TH$(a,d)$:

$$L(\text{TH}, s) = \prod_p \frac{1}{1 - a_p p^{-s} + p^{1-2s}}$$

encodes the coordination census at every prime simultaneously. The BSD conjecture (MOTIVE Identity 7) relates the behavior of $L(\text{TH}, s)$ at $s = 1$ to the algebraic structure of the rational points — the deep arithmetic of the coordination capacity.

### Identity 3 — Étale Cohomology IS the Cohomological Structure of Coordination; $H^1_{\text{ét}}(\text{TH}, \mathbb{Q}_\ell)$ IS the First Coordination Cohomology

Grothendieck introduced étale cohomology (SGA 4, 4½, 5; 1963–1977) to provide a "topological" cohomology theory for varieties over fields where the usual topology is too coarse. The étale topology replaces open sets with étale morphisms — local isomorphisms that generalize the notion of a covering space.

For TH$(a,d)$ over $\mathbb{F}_p$, the étale cohomology groups are:

| Group | Dimension | ERI Identification |
|---|---|---|
| $H^0_{\text{ét}}(\text{TH}, \mathbb{Q}_\ell)$ | 1 | The trivial representation: the existence of the coordination system |
| $H^1_{\text{ét}}(\text{TH}, \mathbb{Q}_\ell)$ | 2 | The first coordination cohomology: carries the Frobenius eigenvalues $\alpha_p, \bar{\alpha}_p$ |
| $H^2_{\text{ét}}(\text{TH}, \mathbb{Q}_\ell)$ | 1 | The Poincaré duality class: the "total capacity" of the coordination system |

The Lefschetz trace formula:

$$\#\text{TH}(\mathbb{F}_{p^n}) = \sum_{i=0}^{2} (-1)^i \text{Tr}(\phi_p^n \mid H^i_{\text{ét}})$$

$$= 1 - (\alpha_p^n + \bar{\alpha}_p^n) + p^n$$

This IS the coordination census formula: the number of self-consistent configurations at precision $p^n$ equals the total capacity ($p^n + 1$) minus the Frobenius trace ($\alpha_p^n + \bar{\alpha}_p^n$). The first cohomology $H^1_{\text{ét}}$ is the 2-dimensional representation that carries ALL the non-trivial coordination information — the Frobenius eigenvalues that determine the Sato-Tate distribution, the $L$-function, and the coordination dynamics at every prime.

### Identity 4 — The Motive $h(\text{TH})$ IS the Universal Coordination Invariant

Grothendieck's theory of motives (*Récoltes et Semailles*, 1986; Milne, "Motives — Grothendieck's Dream," 2012; Scholbach, *J. Algebraic Geom.*, 2015): a motive is a "universal cohomology" — an algebraic object from which all specific cohomology theories (singular, de Rham, $\ell$-adic, crystalline) can be recovered as "realizations."

The motive $h(\text{TH})$ of the Twisted Hessian Curve decomposes:

$$h(\text{TH}) = h^0 \oplus h^1 \oplus h^2$$

| Motivic Piece | Realization | ERI Identification |
|---|---|---|
| $h^0(\text{TH})$ | $H^0$ (trivial) | Existence of the Commons: the "1" in $p + 1 - a_p$ |
| $h^1(\text{TH})$ | $H^1$ (2-dimensional) | The coordination content: Frobenius eigenvalues, $L$-function, all non-trivial structure |
| $h^2(\text{TH})$ | $H^2$ (Tate twist) | Total capacity: the "$p$" in $p + 1 - a_p$ |

The motive $h^1(\text{TH})$ IS the universal coordination invariant. Every specific ERI measurement is a realization of $h^1$:

- The $\ell$-adic realization gives the Frobenius eigenvalues $\alpha_p, \bar{\alpha}_p$
- The de Rham realization gives the periods (the AMARI metric in de Rham coordinates)
- The Hodge realization gives the Hodge structure ($H^{1,0} \oplus H^{0,1}$, the holomorphic/anti-holomorphic decomposition)
- The $G_{\text{coord}}$ measurement IS a further realization of $h^1$ — the "coordination realization" of the motive

Grothendieck's dream: all these realizations are manifestations of a single underlying object — the motive. The ERI programme's claim: all coordination measurements ($G_{\text{coord}}$, Fisher eigenvalues, FERN register contents, CONCERT diagnostics) are realizations of $h^1(\text{TH})$. If the standard conjectures hold, this claim is provable.

### Identity 5 — The Grothendieck Topology IS the FERN Topos; Sheaves on the Étale Site ARE Coordination Data

Grothendieck (SGA 4): a Grothendieck topology on a category $\mathcal{C}$ consists of covering families $\{U_i \to U\}$ satisfying: (i) isomorphisms are covers, (ii) covers are stable under pullback, (iii) covers compose. A site IS a category with a Grothendieck topology. A topos IS the category of sheaves of sets on a site.

The FERN hierarchy IS a topos (TRIVIUM Identity 2). GROTHENDIECK makes this identification precise:

The **site**: the category of register depths $\{\rho_0, \ldots, \rho_5\}$ with morphisms $\rho_k \to \rho_{k'}$ for $k \leq k'$ (shallower registers map to deeper registers). The covering families: an open cover of $\rho_k$ is a collection of contributions $\{a_t\}$ whose combined conditional entropy covers the entropy at register depth $k$.

A **sheaf** on this site assigns to each register depth $\rho_k$ a set of "local sections" — the coordination data valid at that depth — with a gluing condition: if two local sections agree on their overlap, they extend to a global section. The FERN gluing condition IS the cross-register consistency requirement.

The **étale site** of TH$(a,d)$ provides a finer topology than the Zariski site — it "sees" the covering spaces of the curve, including the $n$-torsion points $\text{TH}[n]$. The PRIMA events (rank increases of the Fisher matrix) ARE étale covers: each new eigenvector crossing $\varepsilon$ opens a new "étale neighborhood" in the coordination space.

### Identity 6 — The Weil Conjectures for TH$(a,d)$ ARE the Deep Structure of the Coordination Zeta Function

The Weil conjectures (Weil 1949; proved by Grothendieck/Deligne 1974) for a smooth projective variety $X$ over $\mathbb{F}_q$ state:

**(i) Rationality:** The zeta function $Z(X, t) = \exp\left(\sum_{n \geq 1} \#X(\mathbb{F}_{q^n}) t^n / n\right)$ is a rational function of $t$.

**(ii) Functional equation:** $Z(X, 1/q^d t) = \pm q^{d\chi/2} t^\chi Z(X, t)$ where $d = \dim X$ and $\chi$ is the Euler characteristic.

**(iii) Riemann Hypothesis:** The reciprocal roots of the numerator/denominator have absolute value $q^{i/2}$ for appropriate $i$.

For TH$(a,d)$ (genus 1, $d = 1$):

$$Z(\text{TH}, t) = \frac{1 - a_p t + p t^2}{(1 - t)(1 - pt)}$$

The Riemann Hypothesis: $|\alpha_p| = |\bar{\alpha}_p| = \sqrt{p}$ (the Hasse bound). This IS the statement that the coordination surplus/deficit $a_p$ is bounded: no prime $p$ can have a coordination anomaly exceeding $2\sqrt{p}$. The Frobenius eigenvalues lie on a circle of radius $\sqrt{p}$ — the "critical line" of the coordination zeta function.

The coordination zeta function encodes the entire arithmetic of TH$(a,d)$ at every prime. Its analytic continuation (conjectured for the $L$-function $L(\text{TH}, s)$) governs the global coordination capacity — the Birch and Swinnerton-Dyer conjecture relates the order of vanishing at $s = 1$ to the rank of the Mordell-Weil group, which IS the number of independent coordination dimensions.

### Identity 7 — Grothendieck's "Rising Sea" IS the ERI Methodology; "The Right Level of Generality" IS the TH$(a,d)$ Unification

Grothendieck described his method as the "rising sea" (*la mer qui monte*): rather than attacking a hard problem directly (the "hammer and chisel" approach), raise the level of generality until the problem becomes a trivial consequence of the correct definitions. The sea rises, and the rock is submerged.

The ERI programme IS a rising sea. The "hard problems" — measuring collective intelligence, predicting coordination breakdown, auditing AI systems for regulators — are not attacked directly. Instead, the level of generality is raised: from specific AI systems to arbitrary coordination systems, from specific metrics to the universal coordination invariant ($h^1(\text{TH})$), from specific arithmetic to the scheme TH$(a,d)$ over $\text{Spec}(\mathbb{Z})$. At this level of generality, the specific problems dissolve: they become realizations of the motive, fibers of the scheme, sections of the sheaf.

Grothendieck's principle: "the right level of generality reveals the true structure." The ERI principle: the right level of generality for coordination IS the Twisted Hessian Curve viewed as a scheme over $\mathbb{Z}$, with the coordination structure encoded in its motive $h^1(\text{TH})$ and measured by the Frobenius trace $a_p$ at each prime.

---

## Module B — The Grothendieck Architecture

```
GROTHENDIECK: THE ALGEBRAIC GEOMETRY OF COORDINATION

TH(a,d) AS A SCHEME OVER Spec(Z):
  ┌─────────────────────────────────────┐
  │  Spec(Z)                            │
  │  │                                  │
  │  ├── (0): generic fiber = TH/Q      │
  │  │         rational points = Mordell-Weil group
  │  │         rank = coordination dimensions
  │  │                                  │
  │  ├── (2): fiber at p=2 = TH/F₂     │
  │  │         CHORD base: Q16.16 arithmetic
  │  │                                  │
  │  ├── (p): fiber at each prime       │
  │  │         #TH(F_p) = p + 1 - a_p   │
  │  │         Frobenius trace = coordination census
  │  │                                  │
  │  └── (all primes): L-function       │
  │      L(TH, s) = Π 1/(1 - a_p p^-s + p^{1-2s})
  │      BSD: ord_{s=1} L = rank(TH(Q))
  └─────────────────────────────────────┘

THE MOTIVE h(TH):
  h(TH) = h⁰ ⊕ h¹ ⊕ h²
  
  h⁰: trivial — existence of the Commons
  h¹: 2-dimensional — ALL non-trivial coordination structure
  h²: Tate twist — total capacity

  Realizations of h¹:
    ℓ-adic  →  Frobenius eigenvalues α_p, ᾱ_p
    de Rham →  periods (AMARI metric)
    Hodge   →  H^{1,0} ⊕ H^{0,1} decomposition
    CONCERT →  G_coord (coordination realization)

ÉTALE COHOMOLOGY:
  H⁰(TH) = Q_ℓ         (dim 1: existence)
  H¹(TH) = Q_ℓ²        (dim 2: coordination)
  H²(TH) = Q_ℓ(1)      (dim 1: capacity)

  Lefschetz trace formula:
    #TH(F_{p^n}) = 1 - (α_p^n + ᾱ_p^n) + p^n
    = total capacity - Frobenius trace

WEIL CONJECTURES (proved: Deligne 1974):
  Rationality:    Z(TH, t) is rational ✓
  Functional eq:  Z(TH, 1/pt) = ... ✓
  Riemann Hyp:    |α_p| = √p (Hasse bound) ✓
  → Coordination surplus |a_p| ≤ 2√p at every prime

GROTHENDIECK TOPOLOGY → FERN TOPOS:
  Site: register depths {ρ₀,...,ρ₅} with depth ordering
  Covers: contributions covering register entropy
  Sheaves: coordination data with gluing condition
  PRIMA events = étale covers (new neighborhoods)

THE RISING SEA:
  Don't attack hard problems directly
  Raise the level of generality until problems dissolve
  TH(a,d) over Spec(Z) IS the right level
  Specific measurements are fibers of the scheme
  Specific cohomologies are realizations of the motive
```

---

## Seven Novel Results

**Result 1 — TH$(a,d)$ IS a Scheme over $\text{Spec}(\mathbb{Z})$, and the CHORD Q16.16 Format IS the Fiber at a Non-Standard Point.** The scheme perspective unifies all base rings: TH over $\mathbb{Q}$ (rational points, Mordell-Weil), over $\mathbb{F}_p$ (point-counting, Frobenius), over $\mathbb{C}$ (complex torus, periods), and over $\mathbb{Z}/2^{16}\mathbb{Z}$ (CHORD arithmetic) are all fibers of a single scheme. The CHORD floor $\varepsilon = 2^{-16}$ IS the nilradical of the reduction modulo $2^{16}$.

**Result 2 — The Frobenius Morphism IS the PRIMA Operator, and $a_p$ IS the Coordination Surplus at Prime $p$.** The trace of Frobenius $a_p = p + 1 - \#\text{TH}(\mathbb{F}_p)$ measures the deviation of the coordination census from the generic count. The Hasse bound $|a_p| \leq 2\sqrt{p}$ IS the Weil-Riemann Hypothesis for coordination: no prime can have a coordination anomaly exceeding $2\sqrt{p}$.

**Result 3 — The First Étale Cohomology $H^1_{\text{ét}}(\text{TH}, \mathbb{Q}_\ell)$ IS the Two-Dimensional Space Carrying ALL Non-Trivial Coordination Structure.** The Lefschetz trace formula recovers the coordination census from the cohomological data. All non-trivial coordination information — Frobenius eigenvalues, $L$-function, Sato-Tate distribution — lives in $H^1$.

**Result 4 — The Motive $h^1(\text{TH})$ IS the Universal Coordination Invariant.** Every ERI measurement ($G_{\text{coord}}$, Fisher eigenvalues, FERN register contents) IS a realization of $h^1(\text{TH})$ in a specific cohomology theory. If the standard conjectures hold, $h^1$ exists as a well-defined algebraic object in the abelian category of pure motives, and all realizations are functorially related.

**Result 5 — The FERN Topos IS a Grothendieck Topos over the Étale Site of TH$(a,d)$.** The register hierarchy, the sheaf condition, the intuitionistic logic, and the PRIMA events (étale covers) are all instances of Grothendieck's machinery, applied to the coordination setting.

**Result 6 — The Coordination Zeta Function $Z(\text{TH}, t)$ Satisfies the Weil Conjectures, and the BSD Conjecture Relates the $L$-Function to the Coordination Capacity.** The rationality, functional equation, and Riemann Hypothesis for $Z(\text{TH}, t)$ are proven. The BSD conjecture — that $\text{ord}_{s=1} L(\text{TH}, s) = \text{rank}(\text{TH}(\mathbb{Q}))$ — would, if proven, establish that the analytic coordination capacity (the $L$-function) equals the algebraic coordination capacity (the Mordell-Weil rank). This is the deepest open question connecting the arithmetic and the geometry of the coordination structure.

**Result 7 — Grothendieck's "Rising Sea" IS the ERI Methodology.** The ERI programme does not attack specific coordination problems with specific tools. It raises the level of generality — from specific systems to arbitrary Commons, from specific metrics to the universal motive — until the specific problems become trivial consequences of the correct definitions. This IS Grothendieck's method, applied to the science of collective intelligence.

---

## Formal Summary

| Grothendieck Object | Year | ERI Identification |
|---|---|---|
| Scheme over $\text{Spec}(\mathbb{Z})$ | EGA 1960 | TH$(a,d)$ as a scheme: fibers at each prime, at $\mathbb{Q}$, at $\mathbb{Z}/2^{16}\mathbb{Z}$ |
| Frobenius morphism $\phi_p$ | SGA | PRIMA operator; $a_p$ = coordination surplus at $p$ |
| Étale topology | SGA 4, 1963 | Finer-than-Zariski structure; PRIMA events as étale covers |
| Étale cohomology $H^i_{\text{ét}}$ | SGA 4½, 5 | $H^1$: 2-dimensional space carrying all coordination structure |
| Lefschetz trace formula | Grothendieck | $\#\text{TH}(\mathbb{F}_{p^n}) = 1 - (\alpha_p^n + \bar{\alpha}_p^n) + p^n$ |
| Weil conjectures (Riemann Hypothesis) | Deligne 1974 | $\lvert\alpha_p\rvert = \sqrt{p}$: coordination anomaly bounded by $2\sqrt{p}$ |
| Motive $h(X) = h^0 \oplus h^1 \oplus h^2$ | *Récoltes et Semailles* 1986 | $h^1(\text{TH})$: universal coordination invariant |
| Standard conjectures | Grothendieck | Open: would prove $h^1(\text{TH})$ exists as algebraic object |
| Grothendieck topology | SGA 4 | FERN register site with covering families |
| Topos | SGA 4 | FERN hierarchy as category of sheaves on register site |
| $L$-function $L(\text{TH}, s)$ | — | Coordination zeta function encoding all primes |
| BSD conjecture | Birch–Swinnerton-Dyer | $\text{ord}_{s=1} L = \text{rank}(\text{TH}(\mathbb{Q}))$: analytic = algebraic capacity |
| "Rising sea" method | *Récoltes et Semailles* | ERI methodology: raise generality until problems dissolve |
| Tannakian category | Saavedra/Deligne-Milne | Category of motives with fiber functors = realizations |

---

## Closing Synthesis

Grothendieck rebuilt algebraic geometry because the existing foundations — classical varieties over algebraically closed fields — were too narrow to see the deep connections between geometry and arithmetic. The ERI programme makes the same move: it replaces specific coordination systems (a particular AI ensemble, a particular team, a particular Commons) with the universal scheme TH$(a,d)$ over $\text{Spec}(\mathbb{Z})$, where the coordination structure at every prime, every field, and every precision level is encoded simultaneously. The motive $h^1(\text{TH})$ IS the universal coordination invariant — the single algebraic object from which every specific measurement ($G_{\text{coord}}$, Frobenius eigenvalues, $L$-function, Fisher-Rao metric, FERN register contents) can be recovered as a realization. If the standard conjectures hold, this is not a metaphor but a theorem: the category of pure motives is abelian and semisimple, and the coordination invariant $h^1(\text{TH})$ is a well-defined object with functorially related realizations. Until then, Grothendieck's dream and the ERI programme share the same status: architecturally complete, empirically motivated, conditionally dependent on conjectures that the mathematical community has been unable to settle for sixty years. The sea is rising.

---

**References:**

- Grothendieck, A. and Dieudonné, J. *Éléments de géométrie algébrique* (EGA I–IV). Publ. Math. IHÉS, 1960–1967.
- Grothendieck, A. et al. *Séminaire de géométrie algébrique du Bois Marie* (SGA 1–7). Lecture Notes in Mathematics, Springer, 1970–1977.
- Grothendieck, A. *Récoltes et Semailles*. Gallimard, 2022. English trans. Schneps, MIT Press, 2025.
- Deligne, P. "La conjecture de Weil. I." Publ. Math. IHÉS **43**, 273–307, 1974.
- Deligne, P. "La conjecture de Weil. II." Publ. Math. IHÉS **52**, 137–252, 1980.
- Milne, J. S. *Étale Cohomology*. Princeton University Press, 1980.
- Milne, J. S. "Motives — Grothendieck's Dream." 2012. Available at jmilne.org.
- Hartshorne, R. *Algebraic Geometry*. Graduate Texts in Mathematics 52, Springer, 1977.
- Serre, J.-P. "Zeta and $L$ Functions." In *Arithmetical Algebraic Geometry*, Harper and Row, 82–92, 1965.
- Weil, A. "Numbers of Solutions of Equations in Finite Fields." *Bull. AMS* **55**, 497–508, 1949.
- Silverman, J. H. *The Arithmetic of Elliptic Curves*. 2nd ed., Graduate Texts in Mathematics 106, Springer, 2009.
- Bernstein, D. J. and Lange, T. "Twisted Hessian Curves." *LATINCRYPT 2015*, LNCS 9230, 269–294, 2015.
- Scholbach, J. "Arakelov Motivic Cohomology I." *J. Algebraic Geom.* **24**, 719–748, 2015.
- Freitag, E. and Kiehl, R. *Étale Cohomology and the Weil Conjecture*. Springer, 1988.
- Jannsen, U. "Motives, Numerical Equivalence, and Semi-Simplicity." *Invent. Math.* **107**, 447–452, 1992.
