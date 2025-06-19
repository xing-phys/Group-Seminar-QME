---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://media.hswstatic.com/eyJidWNrZXQiOiJjb250ZW50Lmhzd3N0YXRpYy5jb20iLCJrZXkiOiJnaWZcL21wZW1iYS5qcGciLCJlZGl0cyI6eyJyZXNpemUiOnsid2lkdGgiOjgyOH0sInRvRm9ybWF0IjoiYXZpZiJ9fQ==
# some information about your slides (markdown enabled)
title: Quantum Mpemba Effect
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
hideInToc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# Quantum Mpemba Effect

Thursday's seminar


<!-- <v-drag pos="345,422,320,129">
<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>
</v-drag> -->

<v-drag pos="318,402,313,116">
  <LightOrDark>
    <template #dark>
      <img src="/assets/logo-white.png" alt="Dark mode figure" />
    </template>
    <template #light>
      <img src="/assets/logo-white.png" alt="Light mode figure" />
    </template>
  </LightOrDark>
</v-drag>

<v-drag pos="426,344,135,44">
Ze-Yu, Xing
</v-drag>


<div class="abs-br m-6 text-xl">
  <a href="https://github.com/xing-phys/Group-Seminar-QME" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: default
hideInToc: true
---

# Table of Contents

<style>
.toc-container {
  column-count: 2;
  column-gap: 1rem;
}
.toc-container ul {
  list-style-type: none;
  padding-left: 0;
  margin: 0;
}
.toc-container li {
  break-inside: avoid; /* Prevents list items from breaking across columns */
  margin-bottom: 0.5rem;
}
</style>

<div class="toc-container">
  <Toc />
</div>

---
transition: fade
dragPos:
  bib: 676,495,300,62
---

# Background

<v-drag pos="53,108,611,393">
<img src="/assets/MP.png"/>
</v-drag>

<v-drag pos="bib">
<span style="font-family: 'Georgia', serif; font-size: 12px;">

A. Kumar and J. Bechhoefer, [Nature **584**, 64 (2020)](https://www.nature.com/articles/s41586-020-2560-x)

</span>
</v-drag>

<v-drag pos="701,119,194,74">
  <div v-click="[1, 2]" v-motion
    :initial="{ x: -150 }"
    :enter="{ x: 0 }"
    :leave="{ x: 50 }"
  >

  <span style="font-family: 'Chalkduster'; font-size: 35px;">

  Distance?

  </span>
  </div>
</v-drag>

---
level: 2
---

# Quantifying Distance from Equilibrium

<v-clicks>

- Trace distance: ^[S. Aharony Shapira _et al._, [Phys. Rev. Lett. **133**, 010403 (2024)](https://link.aps.org/doi/10.1103/PhysRevLett.133.010403), J. Zhang _et al._, [Nat Commun **16**, 301 (2025)](https://www.nature.com/articles/s41467-024-54303-0)]
$$
d _{\mathrm{Tr}}(\rho(t)) = \frac{1}{2} \mathrm{Tr}\sqrt{ A^{\dagger}A }, \quad \text{where } A = \rho(t) - \rho_{ss}
$$
- Frobenius distance: ^[F. Carollo _et al._, [Phys. Rev. Lett. **127**, 060401 (2021)](https://link.aps.org/doi/10.1103/PhysRevLett.127.060401)]
$$
d_{\mathrm{F}}(\rho(t)) = \sqrt{ \mathrm{Tr} A^{\dagger}A }
$$
- Quantum relative entropy:
$$
S(\rho(t)| | \rho_{ss}) = \mathrm{Tr}[\rho(t) (\log \rho(t) - \log \rho_{ss})]
$$
- Entanglement asymmetry:
$$
\Delta S^{(n)}_{A} = S^{(n)}(\rho_{A, Q}) - S^{(n)}(\rho_{A})
$$

</v-clicks>

---
transition: fade-out
dragPos:
  bib: 676,495,300,62
---

# Mpemba Effect in Open Quantum Systems
Strong Mpemba

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

F. Carollo _et al._, [Phys. Rev. Lett. **127**, 060401 (2021)](https://link.aps.org/doi/10.1103/PhysRevLett.127.060401)

</v-drag>

<v-drag pos="72,131,819,330">
<img src="/assets/Fast.png"/>
</v-drag>

<div h-95 />

---
level: 2
dragPos:
  bib: 676,495,300,62
transition: fade
---

# Markovian Open Quantum Dynamics

<v-drag pos="bib">
<span style="font-family: 'Georgia', serif; font-size: 12px;">

F. Carollo _et al._, [Phys. Rev. Lett. **127**, 060401 (2021)](https://link.aps.org/doi/10.1103/PhysRevLett.127.060401)

</span>
</v-drag>

<v-click>

<v-drag pos="209,86,520,65">
  <span style="font-size: 16px;">

$$
\dot{\rho}(t) = \mathcal{L}[\rho(t)] \quad \mathrm{Tr}(\mathcal{L}[X]) = 0, \quad \mathcal{L}[X^{\dagger}] = (\mathcal{L}[X])^{\dagger}, \quad \forall X
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="512,137,437,164">
  <span style="font-size: 16px;">

$$
\begin{aligned}
\mathcal{L}^{\dagger}[O] &= i [H, O] + \sum_{\mu=1}^{N_{J}} \left( L^{\dagger}_{\mu} O L_{\mu} - \frac{1}{2} \left\{ O, L^{\dagger}_{\mu}L_{\mu} \right\} \right)\\
\mathcal{L}^{\dagger}[\ell_{k}] &= \lambda_{k}\ell_{k}
\end{aligned}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="43,138,451,138">
  <span style="font-size: 16px;">

$$
\begin{aligned}
  \mathcal{L}[X] &= -i [H, X] + \sum_{\mu=1}^{N_{J}} \left( L_{\mu}XL^{\dagger}_{\mu} - \frac{1}{2} \left\{ L^{\dagger}_{\mu}L_{\mu}, X \right\}  \right) \\
\mathcal{L}[r_{k}] &= \lambda_{k}r_{k} \\
\end{aligned}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="774,241,193,272">
  <span style="font-size: 14px;">

$$
\begin{aligned}
r_{k} &= \sum_{j} c^{k}_{j} x_{j} \\
\ell_{k} &= \sum_{i} d^{k}_{i} x^{\dagger}_{i} \\
L_{ij} &= \mathrm{Tr}(x^{\dagger}_{i} \mathcal{L}[x_{j}]) \\
L^{\dagger}_{ij} &= \mathrm{Tr}(x^{\dagger}_{i} \mathcal{L}^{\dagger}[x_{j}]) \\
L^{\dagger}_{ij} &= L^{\ast}_{ji} \\
&= \mathrm{Tr}(x^{\top}_{j}\mathcal{L}[x_{i}]^{\ast}) \\
&= \mathrm{Tr}(\mathcal{L}[x^{\dagger}_{i}]x_{j})
\end{aligned}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="288,220,197,71">
  <span style="font-size: 20px; color: rgb(0, 0, 255);">

$$
\mathrm{Tr}(\ell_{k}r_{h}) = \delta_{kh}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="456,283,310,106">
  <span style="font-size: 16px;">

$$
\ell_{1} = \mathbb{I} \implies \lambda_{1}=0, \quad \mathrm{Tr}(r_{1}) = 1
$$
$$
\lvert \mathrm{Re}(\lambda_{1}) \rvert \leq \lvert \mathrm{Re}(\lambda_{2}) \rvert \leq \dots 
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="68,275,259,139">
  <span style="font-size: 16px;">

$$
\begin{aligned}
\begin{aligned}
\rho_{0} &= \sum_{k} \mathrm{Tr}(\ell_{k} \rho_{0}) r_{k} \\
&= r_{1} + \sum_{k>1} \mathrm{Tr}(l_{k}\rho_{0})r_{k}
\end{aligned}
\end{aligned}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="490,407,189,70">
  <span style="font-size: 16px;">

$$
\rho_{\mathrm{SS}} = \lim_{ t \to \infty } \rho(t)
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="65,400,393,93">
  <span style="font-size: 20px;">

$$
e^{ t \mathcal{L} }[\rho_{0}] = r_{1} + \sum_{k>1} e^{ t \lambda_{k} } \mathrm{Tr}(\ell_{k} \rho_{0}) r_{k}
$$

  </span>
</v-drag>

</v-click>

---
level: 2
dragPos:
  bib: 676,495,300,62
transition: fade
---

# Mpemba Effect
Suppose $\lambda_{2}$ is real and unique (thus $r_{2}$ and $\ell_{2}$ are Hermitian).

<v-drag pos="bib">
<span style="font-family: 'Georgia', serif; font-size: 12px;">

F. Carollo _et al._, [Phys. Rev. Lett. **127**, 060401 (2021)](https://link.aps.org/doi/10.1103/PhysRevLett.127.060401)

</span>
</v-drag>

<v-drag pos="540,25,319,78">
  <span style="font-size: 16px;">

$$
e^{ t \mathcal{L} }[\rho_{0}] = r_{1} + \sum_{k>1} e^{ t \lambda_{k} } \mathrm{Tr}(\ell_{k} \rho_{0}) r_{k}
$$

  </span>
</v-drag>

<v-click>

<v-drag pos="74,96,135,100">
  <span style="font-size: 20px;">

$$
\tau \sim \frac{1}{\lvert \lambda_{2} \rvert }
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="206,100,360,98">
  <span style="font-size: 20px;">

$$
\mathrm{Tr} (\ell_{2}\rho_{0}) = 0 \implies \tau \sim \frac{1}{\lvert \mathrm{Re}(\lambda_{3}) \rvert }
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="75,174,134,65">
  <span style="font-size: 15px;">

$$
\rho_{0} = \ket{\psi}\bra{\psi} 
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="232,170,238,77">
  <span style="font-size: 20px; color: rgb(180, 50, 30)">

$$
\mathrm{Tr} (\ell_{2} U \rho_{0} U^{\dagger}) = 0
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="40,227,238,77">
  <span style="font-size: 20px;">

$$
\ell_{2} = \sum_{k} \alpha_{k} \ket{\varphi_{k}} \bra{\varphi_{k}}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="303,226,285,94">
  <span style="font-size: 20px;">

  Auxiliary orthonormal basis $\left\{ \ket{\psi_{k}}  \right\}$ with $\ket{\psi} = \ket{\psi_{1}}$.

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="60,313,496,69">
  <span style="font-size: 20px;">

$$
\mathrm{Tr}(\ell_{2} U \rho_{0} U^{\dagger}) = \sum_{k} \alpha_{k} \braket{ \psi_{1} | U^{\dagger} | \varphi_{k} } \braket{ \varphi_{k} | U | \psi_{1} }
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="171,398,213,61">
  <span style="font-size: 12px; color: rgb(155, 155, 155);">

$$
U = U_{1} U_{2}, \quad U_{1} = \sum_{k} \ket{\varphi_{k}} \bra{\psi_{k}}
$$

  </span>
</v-drag>

</v-click>

<div v-after>

<v-drag-arrow pos="158,385,0,90" color="rgb(155, 155, 155)" />

</div>

<v-click>

<v-drag pos="70,455,488,87">
  <span style="font-size: 20px;">

$$
\mathrm{Tr}(\ell_{2} U \rho_{0} U^{\dagger}) = \sum_{k} \alpha_{k} \braket{ \varphi_{1} | U_{2}^{\dagger} | \varphi_{k} } \braket{ \varphi_{k} | U_{2} | \varphi_{1} }
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="614,101,318,90">
  <span style="font-size: 15px;">

$$
\left\{ 
\begin{aligned}
&\mathrm{Tr}(\ell_{2}r_{1}) = 0, \\
&r_{1}\text{ positive}
\end{aligned}
\right. \implies 
\left\{ 
\begin{aligned}
&\alpha_{k_{1}} \cdot \alpha_{k_{2}} <0\\
&\alpha_{k_0} = 0
\end{aligned}
\right.
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="610,172,317,71">
  <span style="font-size: 20px;">

$$
F = \ket{\varphi_{1}} \bra{\varphi_{n}} + \ket{\varphi_{n}} \bra{\varphi_{1}}
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="642,258,206,77">
  <span style="font-size: 20px;">

$$
U_2(s) := e^{ -isF }
$$

  </span>
</v-drag>

</v-click>

<v-click>

<v-drag pos="655,339,268,64">
  <span style="font-size: 15px; color: rgb(155, 155, 155);">

$$
1 + [\cos(s) - 1] F^{2} - i \sin(s) F
$$

  </span>
</v-drag>

</v-click>

<div v-after>

<v-drag pos="699,311,40,62,90">
  <span style="font-size: 20px; color: rgb(155, 155, 155);">

  $=$

  </span>
</v-drag>

</div>

<div v-after>

<v-drag-arrow pos="653,235,0,230" color="rgb(155, 155, 155)" />

</div>

<v-click>

<v-drag pos="534,457,296,77">
  <span style="font-size: 20px;">

$$
= \alpha_{1} \cos ^{2}(s) + \alpha_{n} \sin ^{2}(s)
$$

  </span>
</v-drag>

</v-click>

---
level: 2
transition: fade
dragPos:
  bib: 676,495,300,62
---

# Application I
Dissipative Dicke model

<v-drag pos="12,217,675,302">
<img src="/assets/Dicke_Mpemba.png"/>
</v-drag>

<v-drag pos="bib">
<span style="font-family: 'Georgia', serif; font-size: 12px;">

F. Carollo _et al._, [Phys. Rev. Lett. **127**, 060401 (2021)](https://link.aps.org/doi/10.1103/PhysRevLett.127.060401)

</span>
</v-drag>

<v-drag pos="294,9,522,86">
  <span style="font-size: 18px;">

$$
H = \Omega S_{z} + \omega a^{\dagger}a + \frac{g}{\sqrt{ N }} (a + a ^{\dagger}) S_{x}, \quad L_{1} = \sqrt{ \kappa }a
$$

  </span>
</v-drag>

<v-drag pos="357,69,134,71">
  <span style="font-size: 12px; color: rgb(155, 155, 155);">

$$
\frac{d}{dt} a = \mathcal{L}^{\dagger}[a] = 0
$$

  </span>
</v-drag>

<v-drag-arrow pos="374,68,-69,60" color="rgb(155, 155, 155)" />

<v-drag pos="41,125,522,86">
  <span style="font-size: 18px;">

$$
\tilde{H} = \Omega S_{z} - \frac{4\omega g^{2}}{4\omega^{2} + \kappa^{2}} \frac{S_{x}^{2}}{N}, \quad \tilde{L}_{1} = \frac{2\lvert g \rvert \sqrt{ \kappa }}{\sqrt{ 4 \omega^{2} + \kappa^{2} }} \frac{S_{x}}{\sqrt{ N }}
$$

  </span>
</v-drag>

<v-drag pos="569,92,199,68">
  <span style="font-size: 14px;">

$$
S^{2} = S^{2}_{x} + S^{2}_{y} + S^{2}_{z}
$$

  </span>
</v-drag>

<v-drag pos="749,82,199,68">
  <span style="font-size: 14px;">

$$
S^{2} = \frac{N(N+2)}{4}
$$

  </span>
</v-drag>

<v-drag pos="565,152,199,68">
  <span style="font-size: 14px;">

$$
S_{z}\ket{m} = m \ket{m}
$$

  </span>
</v-drag>

<v-drag pos="744,143,216,70">
  <span style="font-size: 14px;">

$$
m = -\frac{N}{2}, -\frac{N}{2}+1, \dots, \frac{N}{2}
$$

  </span>
</v-drag>

<v-drag pos="701,304,245,74">
  <span style="font-size: 18px;">

$$
\ket{\psi} \propto \sum_{m}(a_{m} + i b_{m}) \ket{m}
$$

  </span>
</v-drag>

<v-drag pos="725,397,199,68">
  <span style="font-size: 18px;">

$$
a_{m}, b_{m} \in [0,1]
$$

  </span>
</v-drag>

<v-drag pos="576,200,270,80">
  <span style="font-size: 18px;">

$$
= \left\{ \mathrm{Tr}(e^{ t\mathcal{L} }[\rho(t)] - \rho_{\text{SS}})^{2} \right\}^{1/2}
$$

  </span>
</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
transition: fade
---

# Application II
Interacting spin model

<v-drag pos="bib">
<span style="font-family: 'Georgia', serif; font-size: 12px;">

F. Carollo _et al._, [Phys. Rev. Lett. **127**, 060401 (2021)](https://link.aps.org/doi/10.1103/PhysRevLett.127.060401)

</span>
</v-drag>

<v-drag pos="101,140,792,360">
<img src="/assets/Rydberg_Mpemba.png"/>
</v-drag>

<v-drag pos="340,28,467,103">
  <span style="font-size: 20px;">

$$
H = \Omega S_{x} - \Delta S_{z} + \frac{V}{N} S^{2}_{z}, \quad L_{1} = \sqrt{ \frac{\kappa}{N} } S_{-}
$$

  </span>
</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: -16,0,0,0
---

# Experimental Observation
Observation of strong Mpemba effect

<v-drag pos="bib">
<span style="font-family: 'Georgia', serif; font-size: 12px;">

J. Zhang _et al._, [Nat Commun **16**, 301 (2025)](https://www.nature.com/articles/s41467-024-54303-0)

</span>
</v-drag>

<v-drag pos="353,58,608,92">
  <span style="font-size: 18px;">

$$
H = \sum_{j=1,2} \frac{\Omega_{j}}{2}(\ket{0} \bra{j} + \ket{j} \bra{0} ), \quad L_{j} = \sqrt{ \kappa_{j} } \ket{0} \bra{j} \, (j = 1, 2)
$$

  </span>
</v-drag>

<img v-drag="'fig'" src="/assets/strong_ex1.png">

<v-click>

<v-drag pos="-57,266,268,81,270">
  <span style="font-size: 18px;">

$$
c_{i}(t) = c_{i}e^{ \lambda_{i} t } = \mathrm{Tr}[L_{i} \rho_{ \text{in}}] e^{ \lambda_{i} t }
$$

  </span>
</v-drag>

</v-click>

<div v-after>

<v-drag pos="143,493,279,74">
  <span style="font-size: 18px; color: rgb(125, 125, 125);">

From strong ME to weak ME

  </span>
</v-drag>

</div>

<div v-after>

<img v-drag="'fig'" src="/assets/strong_ex2.png">

</div>

---
dragPos:
  arrow: -16,0,0,0
  AA: -16,0,0,0
  AA1: -16,0,0,0
transition: fade-out
---

# Quantum Mpemba Effect in Isolated Systems

<v-drag pos="59,85,138,105">
  <div v-click style="font-size: 25px;">

$$
\ket{\psi(0)}
$$

  </div>
</v-drag>

<v-drag pos="-2,231,266,93,90">
  <div v-click style="font-size: 16px; color: rgb(125, 125, 125);">

$$
U(t) = \exp(-iHt)
$$

  </div>
</v-drag>

<div v-after>

<v-drag-arrow pos="110,169,0,240" color="rgb(125, 125, 125)" />

</div>

<v-drag pos="51,397,138,105">
  <div v-click style="font-size: 25px;">

$$
\ket{\psi(t)}
$$

  </div>
</v-drag>

<div v-click>
<img v-drag="'AA'" src="/assets/AA.svg">
</div>

<div v-click>
<img v-drag="'arrow'" src="/assets/arrow.svg">
</div>

<div v-click>
<img v-drag="'AA1'" src="/assets/AA1.svg">
</div>

<v-drag pos="315,169,258,94">
  <div v-click style="font-size: 25px;">

$$
\rho_{A} = \mathrm{Tr}_{\bar{A}}(\ket{\Psi}\bra{\Psi})
$$

  </div>
</v-drag>

<v-drag pos="348,340,199,91">
  <div v-click style="font-size: 25px;">

$$
\rho_{A} \rightsquigarrow \rho_{A, ss}
$$

  </div>
</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 30,97,901,351
transition: fade
---

# Symmetry Restoration

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

F. Ares _et al._, [Nat Commun **14**, 2036 (2023)](https://www.nature.com/articles/s41467-023-37747-8)

</v-drag>

<v-drag pos="54,100,274,85">
  <div v-click style="font-size: 25px;">

$$
\ket{\Psi} \quad \rho_{A} = \mathrm{Tr}_{\bar{A}}(\ket{\Psi}\bra{\Psi})
$$

  </div>
</v-drag>

<v-drag pos="51,173,278,79">
  <div v-click style="font-size: 25px;">

$$
S(\rho_{A}) = - \mathrm{Tr}(\rho_{A}\log \rho_{A})
$$

  </div>
</v-drag>

<v-drag pos="71,249,201,72">
  <div v-click style="font-size: 25px;">

$$
Q = Q_{A} + Q_{\bar{A}}
$$

  </div>
</v-drag>

<v-drag pos="67,329,201,80">
  <div v-click style="font-size: 25px;">

$$
[\rho_{A}, Q_{A}] \neq 0
$$

  </div>
</v-drag>

<v-drag pos="fig">
<div v-click="[6, 7]" style="font-family: 'Chalkduster'; font-size: 35px;" v-motion
  :initial="{ x: -150, y: -50 }"
  :enter="{ x: 0, y: 0 }"
  :leave="{ x: 50, y: 50 }"
>

<img src="/assets/rho.png">

</div>
</v-drag>

<v-drag pos="63,407,201,98">
  <div v-click style="font-size: 25px;">

$$
\rho_{A, Q} = \sum_{q \in \mathbb{Z}} \Pi_{q}\rho_{A} \Pi_{q}
$$

  </div>
</v-drag>

<v-drag pos="413,106,438,71">
  <div v-click=7 style="font-size: 30px;">

  Entanglement asymmetry (EA):

  </div>
</v-drag>

<v-drag pos="422,150,454,153">
  <div v-click=7 style="font-size: 25px;">

$$
\begin{aligned}
\Delta S_{A} &= S(\rho_{A,Q}) - S(\rho_{A}) \\
&= \mathrm{Tr} (\rho_{A}\log \rho_{A}) - \mathrm{Tr} (\rho_{A, Q}\log \rho_{A, Q}) \\
&= \mathrm{Tr} [\rho_{A}(\log \rho_{A} - \log \rho_{A,Q})] \geq 0
\end{aligned}
$$

  </div>
</v-drag>

<v-drag pos="416,312,95,71">
  <div v-click=8 style="font-size: 30px;">

  Note:

  </div>
</v-drag>

<v-drag pos="493,356,302,81">
  <div v-click=8 style="font-size: 25px;">

$$
\Delta S_{A} = 0 \iff \rho_{A, Q} = \rho_{A}
$$

  </div>
</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 32,149,475,385
transition: fade
---

# Entanglement Asymmetry

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

F. Ares _et al._, [Nat Commun **14**, 2036 (2023)](https://www.nature.com/articles/s41467-023-37747-8)

</v-drag>

<v-drag pos="56,92,368,59">
  <div v-click style="font-size: 20px; font-family: 'Arial Black'">

  Rényi entanglement asymmetry

  </div>
</v-drag>

<v-drag pos="49,134,461,92">
  <div v-click style="font-size: 20px;">

$$
\Delta S_{A}^{(n)} = \frac{1}{1-n} [\log \mathrm{Tr}(\rho_{A, Q}^{n}) - \log \mathrm{Tr}(\rho_{A}^{n})]
$$

  </div>
</v-drag>

<v-drag pos="34,205,241,81">
  <div v-click style="font-size: 20px;">

$$
\lim_{ n \to 1 } \Delta S_{A}^{(n)} = \Delta S_{A}
$$

  </div>
</v-drag>

<v-drag pos="47,266,457,100">
  <div v-click style="font-size: 20px;">

$$
\rho_{A, Q} = \sum_{q \in \mathbb{Z}} \Pi_{q}\rho_{A} \Pi_{q} = \int_{-\pi}^{\pi} \frac{\mathrm{d}\alpha}{2\pi} \, e^{ i \alpha Q_{A} }\rho_{A}e^{ i \alpha Q_{A} } 
$$

  </div>
</v-drag>

<v-drag pos="48,352,373,97">
  <div v-click style="font-size: 20px;">

$$
\mathrm{Tr}(\rho_{A, Q}^{n}) = \int_{-\pi}^{\pi} \frac{\mathrm{d}\alpha_{1} \cdots \mathrm{d}\alpha_{n}}{(2\pi)^{n}} \,  Z_{n}(\boldsymbol{\alpha})
$$

  </div>
</v-drag>

<v-drag pos="37,427,337,112">
  <div v-click style="font-size: 20px;">

$$
Z_{n}(\boldsymbol{\alpha}) = \mathrm{Tr}\left[ \prod_{j=1}^{n} \rho_{A} e^{ i \alpha_{j, j+1} Q_{A} } \right]
$$

  </div>
</v-drag>

<v-drag pos="358,441,162,88">
  <div v-after style="font-size: 15px;">

$$
\begin{aligned}
  &\alpha_{ij} = \alpha_{i} - \alpha_{j} \\
  &\alpha_{n+1} = \alpha_{1}
\end{aligned}
$$

  </div>
</v-drag>

<v-drag pos="600,35,347,54">
  <div v-click style="font-size: 20px;">

  # Tilted Ferromagnetic

  </div>
</v-drag>

<v-drag pos="605,79,345,83">
  <div v-after style="font-size: 20px;">

$$
\ket{\theta; \nearrow \nearrow \cdots} = e^{ -i \frac{\theta}{2}\sum_{j}\sigma_{j}^{y} } \ket{\uparrow \uparrow \cdots} 
$$

  </div>
</v-drag>

<v-drag pos="703,135,172,95">
  <div v-click style="font-size: 15px;">

$$
Q = \frac{1}{2} \sum_{j}\sigma_{j}^{z}
$$

  </div>
</v-drag>

<v-drag pos="539,190,428,90">
  <div v-click style="font-size: 15px;">

$$
Z_{n}(\boldsymbol{\alpha}) = \prod_{j}^{n}\left[ i \cos(\theta) \sin\left( \frac{\alpha_{j, j+1}}{2} \right) + \cos\left( \frac{\alpha_{j, j+1}}{2} \right) \right]^{\ell}
$$

  </div>
</v-drag>

<v-drag pos="510,266,462,100">
  <div v-click style="font-size: 15px;">

$$
\Delta S_{A}^{(n)} = \frac{1}{1 - n} \log\left[ \cos ^{2n\ell}\left( \frac{\theta}{2} \right)\sum_{p=0}^{\ell} \begin{pmatrix}
\ell \\
p
\end{pmatrix}^{n} \tan ^{2n\ell}\left( \frac{\theta}{2} \right) \right]
$$

  </div>
</v-drag>

<div v-click>
<img v-drag="'fig'" src="/assets/EA0.png">
</div>

---
level: 2
dragPos:
  bib: 676,495,300,62
  arrow: -16,0,0,0
  fig: 17,101,446,464
  box: 743,30,178,206
transition: fade
---

# Quench Dynamics

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

F. Ares _et al._, [Nat Commun **14**, 2036 (2023)](https://www.nature.com/articles/s41467-023-37747-8)

</v-drag>

<v-drag pos="42,100,432,94">
  <div v-click style="font-size: 20px;">

$$
\ket{\Psi(0)} = \frac{\ket{\theta; \nearrow \nearrow \cdots} - \ket{-\theta; \nearrow \nearrow \cdots} }{\sqrt{ 2 }}
$$

  </div>
</v-drag>

<div v-click>
<img v-drag="'arrow'" src="/assets/arrow.svg">
</div>

<v-drag pos="131,236,288,97">
  <div v-after style="font-size: 16px; color: rgb(125, 125, 125);">

$$
H = -\frac{1}{4} \sum_{j = -\infty}^{\infty} [\sigma_{j}^{x} \sigma_{j+1}^{x} + \sigma_{j}^{y} \sigma_{j+1}^{y}].
$$

  </div>
</v-drag>

<v-drag pos="146,318,157,64">
  <div v-after style="font-size: 16px; color: rgb(125, 125, 125);">

$$
\epsilon(k) = -\cos (k)
$$

  </div>
</v-drag>

<v-drag pos="48,460,208,82">
  <div v-click style="font-size: 20px;">

$$
\ket{\Psi(t)} = e^{ -itH }\ket{\Psi(0)}
$$

  </div>
</v-drag>

<v-drag pos="504,82,218,84">
  <div v-click style="font-size: 20px;">

$$
\Delta S_{A}^{(n)}(t) \simeq \frac{\pi^{2}b(\zeta)\ell}{24}
$$

  </div>
</v-drag>

<v-drag pos="497,187,473,97">
  <div v-click style="font-size: 18px;">

$$
b(\zeta) = \frac{\sin ^{2} \theta}{2} - \int_{0}^{2\pi} \frac{\mathrm{d}k}{2\pi} \, \min(2 \zeta \lvert \epsilon ^{\prime}(k) \rvert , 1)\sin ^{2}\Delta_{k}
$$

  </div>
</v-drag>

<v-drag pos="790,46,105,58">
  <div v-click>
  <span style="font-size: 30px; font-family: 'Bangla MN'">Large</span>
  </div>
</v-drag>

<v-drag pos="788,64,96,112">

  <div v-after style="font-size: 25px;">

$$
\zeta = \frac{t}{\ell}
$$

  </div>
</v-drag>

<v-drag pos="773,41,137,128" style="font-size: 80px; color: transparent">
  <span v-mark.box.orange>aaa</span>
</v-drag>

<v-drag pos="526,279,397,94">
  <div v-click style="font-size: 18px;">

$$
\cos \Delta_{k} = \frac{2 \cos(\theta) - (1+\cos ^{2} \theta)\cos (k)}{1 + \cos ^{2}\theta - 2 \cos(\theta)\cos(k)}
$$

  </div>
</v-drag>

<v-drag pos="475,377,205,60">
  <div v-click style="font-size: 25px; font-family: 'Arial Black'">

Leading term

  </div>
</v-drag>

<v-drag pos="523,413,423,102">
  <div v-after style="font-size: 20px;">

$$
\Delta S_{A}^{(n)}(t) \simeq \frac{\pi}{1152} \left( 1 + 8 \frac{\cos ^{2}\theta}{\sin ^{4}\theta} \right) \frac{\ell}{\zeta^{3}}
$$

  </div>
</v-drag>

<div v-click>
<img v-drag="'fig'" src="/assets/EAt.png">
</div>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 444,42,534,474
transition: fade
---

# Non-Integrable Systems

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

F. Ares _et al._, [Nat Commun **14**, 2036 (2023)](https://www.nature.com/articles/s41467-023-37747-8)

</v-drag>

<img v-drag="'fig'" src="/assets/QME_.png">

<v-drag pos="15,318,419,173" v-after style="font-size: 18px;">

$$
\begin{aligned}
H = &-\frac{1}{4} \sum_{i=1}^{N-1} (\sigma_{i}^{x}\sigma_{i+1}^{x} + \sigma_{i}^{y}\sigma_{i+1}^{y} + \Delta\sigma_{i}^{z}\sigma_{i+1}^{z}) \\
&- \frac{J_{2}}{4}\sum_{i=1}^{N-2} (\sigma_{i}^{x}\sigma_{i+2}^{x} + \sigma_{i}^{y} \sigma_{i+2}^{y} + \Delta_{2} \sigma_{i}^{z} \sigma_{i+2} ^{z})
\end{aligned}
$$

</v-drag>

<v-drag pos="76,171,334,70" v-after style="font-size: 18px;">

$$
\ket{\theta; \nearrow \nearrow \cdots} = e^{ -i \frac{\theta}{2}\sum_{j}\sigma_{j}^{y} } \ket{\uparrow \uparrow \cdots} 
$$

</v-drag>

<v-drag pos="602,63,102,67" v-after style="font-size: 15px;">

$$
J_2 = 0
$$

</v-drag>

<v-drag pos="835,134,102,67" v-after style="font-size: 15px;">

$$
J_2 = 0
$$

</v-drag>

<v-drag pos="870,301,102,67" v-after style="font-size: 15px;">

$$
J_2 = 1
$$

</v-drag>

<v-drag pos="608,301,102,67" v-after style="font-size: 15px;">

$$
J_2 = 1
$$

</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 8,9,807,495
transition: fade
---

# Trapped-Ion Quantum Simulation
Symmetry restoration with a long-range spin-spin interaction

<img v-drag="'fig'" src="/assets/ion.png">

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

L. Kh. Joshi _et al._, [Phys. Rev. Lett. **133**, 010402 (2024)](https://link.aps.org/doi/10.1103/PhysRevLett.133.010402)

</v-drag>

<v-drag pos="51,468,347,92" v-after style="font-size: 18px;">

$$
H_{XY} = \sum_{i>j} \frac{J_{0}}{2 \lvert i - j \rvert ^{\alpha}} (\sigma_{i}^{x} \sigma_{j}^{x} + \sigma_{i} ^{y} \sigma_{j}^{y})
$$

</v-drag>

<v-drag pos="839,44,105,64" v-after style="font-size: 18px;">

$$
N = 12
$$

</v-drag>

<v-drag pos="827,116,139,160" v-after style="font-size: 18px;">

Average all possible subsystems of $N_A = 4$ chosen between 4 and 9

</v-drag>

<v-drag pos="816,320,160,92" v-after style="font-size: 18px;">

Left: Connected 4-quibit subsystems

</v-drag>

<v-drag pos="829,404,125,92" v-after style="font-size: 18px;">

Right: All 4-9 ($C^4_6 = 15$)

</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 40,145,631,346
---

# Disorder Systems

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

L. Kh. Joshi _et al._, [Phys. Rev. Lett. **133**, 010402 (2024)](https://link.aps.org/doi/10.1103/PhysRevLett.133.010402)

</v-drag>

<img v-drag="'fig'" src="/assets/disorder.png">

<v-drag pos="537,39,419,91" v-after style="font-size: 18px;">

$$
H = \sum_{i > j} \frac{J_{0}}{2\lvert i - j \rvert ^{\alpha}} (\sigma_{i}^{x} \sigma_{j}^{x} + \sigma_{i}^{y} \sigma_{j}^{y}) + \sum_{i} h_{i} \sigma_{i} ^{z}
$$

</v-drag>

<v-drag pos="740,142,157,67" v-after style="font-size: 18px;">

$$
h_i \in w(0, J_0)
$$

</v-drag>

<v-drag pos="97,121,157,67" v-after style="font-size: 18px;">

$$
w = 6
$$

</v-drag>

<v-drag pos="399,123,157,67" v-after style="font-size: 18px;">

$$
w = 14
$$

</v-drag>

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

L. Kh. Joshi _et al._, [Phys. Rev. Lett. **133**, 010402 (2024)](https://link.aps.org/doi/10.1103/PhysRevLett.133.010402)

</v-drag>

---
dragPos:
  bib: 676,495,300,62
transition: fade-out
---

# QME without Global Symmetry

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

T. Bhore _et al._, [arXiv:2505.17181](http://arxiv.org/abs/2505.17181)

</v-drag>

<v-drag pos="54,99,465,103" v-after style="font-size: 18px;">
<v-click>

$$
E_{\Psi} = \braket{ \Psi | H | \Psi } = \frac{1}{\mathcal{Z}} \mathrm{Tr}(H e^{ -\beta H }), \quad \mathcal{Z} = \mathrm{Tr}(e^{ -\beta H })
$$

</v-click>
</v-drag>

<v-drag pos="741,32,124,90" v-after style="font-size: 18px;">

<span v-mark.circle.orange>
$$
T = \frac{1}{\beta}
$$
</span>

</v-drag>

<v-drag pos="35,169,346,86" v-after style="font-size: 18px;">
<v-click>

$$
\Delta(\rho^{A})(t) = \frac{1}{2} \lvert \rho^{A}(t) - \rho_{\text{DE}}(\rho^{A}) \rvert
$$

</v-click>
</v-drag>

<v-drag pos="41,245,459,102" v-after style="font-size: 18px;">
<v-click>

$$
\rho_{\text{DE}}(\rho^{A}) = \mathrm{Tr}_{\bar{A}} [\rho_{\text{DE}}] = \sum_{n} \lvert c_{n}^{2} \rvert \mathrm{Tr}_{\bar{A}}(\ket{E_{n}} \bra{E_{n}} )
$$

</v-click>
</v-drag>

<v-drag pos="554,167,332,190" v-after style="font-size: 18px;">
<v-after>

$$
\begin{aligned}
\rho_{\text{DE}} &= \sum_{n}\braket{ E_{n} | \rho(0) | E_{n} } \ket{E_{n}} \bra{E_{n}} \\
&= \sum_{n} \lvert \braket{E_n | \Psi} \rvert ^{2} \ket{E_{n}} \bra{E_{n}} \\
&= \sum_{n} \lvert c_{n}^{2} \rvert \ket{E_{n}} \bra{E_{n}}
  
\end{aligned}
$$

</v-after>
</v-drag>

<v-drag pos="35,330,515,86" v-after style="font-size: 18px;">
<v-click>

$$
\ket{\Psi(t)}\bra{\Psi(t)} = \rho_{\text{DE}} + \sum_{n\neq m} c_{n} c_{m}^{\ast} e^{ -i (E_{n} - E_{m}) t }\ket{E_{n}} \bra{E_{m}} 
$$

</v-click>
</v-drag>

<v-drag pos="36,395,521,119" v-after style="font-size: 18px;">
<v-click>

$$
\Delta(\rho^{A})(t) = \frac{1}{2} \left\lvert  \sum_{n\neq m} c_{n} c_{m}^{\ast} e^{ -i (E_{n} - E_{m})t } \mathrm{Tr}_{B}(\ket{E_{n}} \bra{E_{m}} )  \right\rvert 
$$

</v-click>
</v-drag>

<v-drag pos="294,426,99,62" v-after style="font-size: 18px; color: transparent">
<span v-mark.underline.green>aaaaaaaaa</span>
</v-drag>

<v-drag pos="595,389,287,83" v-after style="font-size: 18px;">

<span v-mark.box.blue>
$$
\text{IPR}(\ket{\Psi} ) = \sum_{n}\lvert \braket{ E_{n} | \Psi }  \rvert ^{4}
$$
</span>

</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig1: -16,0,0,0
  fig2: -16,0,0,0
transition: fade
---

# Mixed-Field Ising Model
Open chain without reflection symmetry

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

T. Bhore _et al._, [arXiv:2505.17181](http://arxiv.org/abs/2505.17181)

</v-drag>

<v-drag pos="56,104,328,184" v-after style="font-size: 18px;">

$$
\begin{aligned}
H^{\text{MFIM}} = &J_{zz} \sum_{i=1}^{N-1} \sigma_{i}^{z}\sigma_{i+1}^{z} \\
+ &h_{x}\sum_{i=1}^{N} \sigma_{i}^{x} + h_{z} \sum_{i=2}^{N-1} \sigma_{i}^{z}
\end{aligned}
$$

</v-drag>

<v-drag pos="84,266,260,60" v-after style="font-size: 16px;">

$$
\delta h_{1}^{z} = 0.25, \quad \delta h_{N}^{z} = -0.25
$$

</v-drag>

<v-drag pos="57,317,340,87" v-after style="font-size: 16px;">

$$
(J_{zz}, h_{z}, h_{x}) = \left( 1, \frac{1 + \sqrt{ 5 }}{4}, \frac{\sqrt{ 5 } + 5}{8} \right)
$$

</v-drag>

<v-drag pos="27,407,445,104" v-after style="font-size: 16px;">

$$
\ket{\theta, \phi} = \bigotimes_{i=1}^{N} \left[ \cos\left( \frac{\theta}{2} \right)\ket{\uparrow}_{i} + e^{ i \phi } \sin \left( \frac{\theta}{2} \right) \ket{\downarrow}_{i} \right]
$$

</v-drag>

<div v-click>
<img v-drag="'fig1'" src="/assets/EN.png">
</div>

<v-drag pos="681,232,97,59" v-after style="font-size: 16px; color: rgb(114, 36, 0);">
<v-after>

$$
N = 14
$$

</v-after>
</v-drag>

<div v-click>
<img v-drag="'fig2'" src="/assets/IPR.png">
</div>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: -16,0,0,0

transition: fade
---

# Random Hamiltonian

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

T. Bhore _et al._, [arXiv:2505.17181](http://arxiv.org/abs/2505.17181)

</v-drag>

<v-drag pos="21,68,477,115" v-after style="font-size: 18px;">

$$
H_{\text{R}} = \sum_{i=1}^{N-1} (\boldsymbol{\sigma}_{i} \times \boldsymbol{\sigma}_{i+1})\cdot \hat{\boldsymbol{v}}_{i} + J_{\text{H}} \sum_{i}^{N-1} \boldsymbol{\sigma}_{i}\cdot \boldsymbol{\sigma}_{i+1}
$$

</v-drag>

<v-drag pos="92,193,296,74" v-after style="font-size: 18px;">

$$
\hat{\boldsymbol{v}}_{i} = (v_{x}, v_{y}, v_{z})_{i} \in [-1, 1]
$$

</v-drag>

<v-drag pos="492,71,477,115" v-after style="font-size: 18px;">

$$
\ket{\psi} = \bigotimes_{i=1}^{N} \left[ \cos\left( \frac{\theta_{i}}{2} \right)\ket{\uparrow}_{i} + e^{ i \phi_{i} } \sin \left( \frac{\theta_{i}}{2} \right) \ket{\downarrow}_{i} \right]
$$

</v-drag>

<v-drag pos="598,190,218,86" v-after style="font-size: 18px;">

$$
\theta_{i} \in \left[ \theta - \frac{f}{2} \pi, \theta + \frac{f}{2} \pi \right]
$$

</v-drag>

<v-drag pos="603,296,212,69" v-after style="font-size: 18px;">

$$
\phi_{i} \in [\phi - f \pi, \phi + f \pi]
$$

</v-drag>

<div v-click>
<img v-drag="'fig'" src="/assets/random.png">
</div>

<v-drag pos="426,467,97,59" v-after style="font-size: 20px; color: rgb(114, 36, 0);">
<v-after>

$$
N = 10
$$

</v-after>
</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 229,199,736,316
transition: fade
---

# Floquet Systems
Without Energy Conservation

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

T. Bhore _et al._, [arXiv:2505.17181](http://arxiv.org/abs/2505.17181)

</v-drag>

<v-drag pos="601,133,224,49">
  <div style="font-size: 20px; color:rgb(0, 70, 4); font-family: 'Bangla MN'">

Kicked Ising Model

  </div>
</v-drag>

<v-drag pos="302,48,687,115" v-after style="font-size: 18px;">

$$
U_{\text{KI}} = \exp\left[ -i T_{1}\left( J_{zz}\sum_{j} \sigma_{j}^{z} \sigma_{j+1}^{z} + h_{z} \sum_{j} \sigma_{j}^{z} \right) \right]\cdot \exp\left[ -i T_{2} h_{x} \sum_{j} \sigma_{j}^{x} \right]
$$

</v-drag>

<v-drag pos="40,133,313,66" v-click style="font-size: 16px;">

$$
\ket{\Psi(A)} = \sum_{\boldsymbol{s}}(\dots A^{[s_{i-1}]}A^{[s_{i}]}A^{[s_{i+1}]})\ket{\boldsymbol{s}} 
$$

</v-drag>

<v-drag pos="359,142,84,63">
  <div v-after style="font-size: 25px; color:rgb(0, 103, 248); font-family: 'Bangla MN'">

iMPS

  </div>
</v-drag>

<v-drag pos="41,237,183,78" v-click style="font-size: 16px;">

$$
A^{[\downarrow]}(\theta) = \begin{pmatrix}
\cos \theta  & 0 \\
\sin \theta  & 0
\end{pmatrix}
$$

</v-drag>

<v-drag pos="38,310,179,82" v-after style="font-size: 16px;">

$$
A^{[\uparrow]}(\theta) = \begin{pmatrix}
0  & -i \\
0 & 0
\end{pmatrix}
$$

</v-drag>

<div v-click>
<img v-drag="'fig'" src="/assets/Floquet.png">
</div>

<v-drag pos="8,461,225,68" v-after style="font-size: 16px;">

$$
S_{E} = - \mathrm{Tr} \rho^{A}(t)\ln \rho^{A}(t)
$$

</v-drag>

<v-drag pos="840,354,97,59" v-after style="font-size: 20px; color: rgb(114, 36, 0);">
<v-after>

$$
N = 10
$$

</v-after>
</v-drag>

---
level: 2
dragPos:
  bib: 676,495,300,62
  fig: 4,90,971,249
transition: fade
---

# Trace Distance vs Entanglement Asymmetry

<v-drag pos="bib" style="font-family: 'Georgia', serif; font-size: 12px;">

T. Bhore _et al._, [arXiv:2505.17181](http://arxiv.org/abs/2505.17181)

</v-drag>

<img v-drag="'fig'" src="/assets/compare.png">

<v-drag pos="26,350,451,185" v-after style="font-size: 20px;">

$$
\begin{aligned}
H &= J_{1} \sum_{i=1}^{N-1} (\sigma_{i}^{x}\sigma_{i+1}^{x} + \sigma_{i}^{y}\sigma_{i+1}^{y} + \Delta_{1}\sigma_{i}^{z}\sigma_{i+1}^{z}) \\
&+ J_{2}\sum_{i=1}^{N-2} (\sigma_{i}^{x}\sigma_{i+2}^{x} + \sigma_{i}^{y} \sigma_{i+2}^{y} + \Delta_{2} \sigma_{i}^{z} \sigma_{i+2} ^{z})
\end{aligned}
$$

</v-drag>

<v-drag pos="520,353,415,115" v-after style="font-size: 20px;">

$$
\ket{\psi(\alpha; \theta)} = \exp\left( -i \frac{\theta}{2} \sum_{i} \sigma_{i}^{\alpha} \right) \ket{\uparrow \uparrow \uparrow \dots}
$$

</v-drag>

<v-drag pos="560,428,134,74" v-after style="font-size: 20px;">

$$
\alpha = x, y
$$

</v-drag>

<v-drag pos="244,316,466,73" v-after style="font-size: 20px; color: rgb(114, 36, 0);">
<v-after>

$$
N = 10, \quad J_1 = J_2 = 1, \quad \Delta_1 = \Delta_2 = 0.5
$$

</v-after>
</v-drag>

---
layout: center
class: 'final-slide'
hideInToc: true
---

# Thank You!

<div class="contact-info">
  <p>Ze-Yu Xing</p>
</div>

<div class="footer">
  <p>Presented at Group Seminar June 2025</p>
</div>