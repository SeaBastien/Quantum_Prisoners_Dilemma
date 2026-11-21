# CPSC 4110 Project Proposal: Quantum Prisoners Dilemma
 Escaping the prisoner’s dilemma with a quantum strategy.

**Authors:** Sabastien Yu, Hunter Secretan  
**Date:** November 20, 2026

## Overview
Eisert, Wilkens, and Lewenstein's claim on the "Prisoner's Dilemma" follows, "this game ceases to pose a dilemma if quantum strategies are allowed for" (Eisert et al., 1999, p. 3077).  
The posed question: Does the quantum strategy Q still beat defection on the IBM device at full entanglement (γ = π/2)? And if not, what is the noise threshold that breaks it?   
Our goal is to test if the Eisert-Wilkens-Lewenstein (EWL) scheme holds against real hardware.
The EWL scheme predicts that (Q, Q) is an equilibreum with a payoff of (3, 3), and choosing QD holds the payoff (5, 0).   

<dl>
    <dd>We will use an IBM quantum computer to test the numeric dichotomy between theory the EWL scheme and the simulated products.</dd>
    <dd>This test will measure the prediction of</dd> 
</dl>


## Background

In the classical prisoner’s dilemma each player chooses to cooperate (C) or defect (D). With
payoffs (3, 3) for CC, (0, 5) for CD, (5, 0) for DC and (1, 1) for DD, defecting is the best reply to everything,
so both defect and both get 1, although both cooperating would give each 3

In the EWL scheme each player owns one Qbit. 
$$
A \space gate \space \space J(\gamma) = \exp\!\left(i\gamma\, D \otimes D / 2\right), \qquad
with \space \space          D = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix},
$$
<!-- ^I love LaTeX syntax so much (this was a pain to figure out) -->

entangles the two Qbits. Each player then applies a one-Qbit strategy 𝑈(𝜃, 𝜙), the gate 𝐽† is applied, and the Qbits are measured. The payoff is the expected payoff over the four outcomes. At full entanglement (𝛾 = 𝜋/2) a new quantum strategy 𝑄 = 𝑈(0, 𝜋/2) appears. Both players choosing 𝑄 is an equilibrium with payoff (3, 3). The dilemma is resolved.

