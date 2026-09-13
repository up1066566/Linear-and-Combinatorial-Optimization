# Linear-and-combinatorial-optimization
This repository contains the full theoretical resolution, graphical code implementations (Python / Matplotlib), and standard Simplex algorithms applied in 6 exercises

## 📋 Table of Contents
* [Overview](#overview)
* [Exercises Summary](#exercises-summary)
* [Tech Stack & Requirements](#tech-stack--requirements)
* [File Structure](#file-structure)
* [Installation & Execution](#installation--execution)

---

## ℹ️ Overview

This project tackles standard optimization topics including linear programming formulation[cite: 13], graphical boundary visualization[cite: 3], convexity proofs, basic feasible solutions (BFS), geometric degeneracy, and Simplex table calculations.

---

## 📐 Exercises Summary

### **Exercise 1: Graphical Solution & Objective Sensitivity**
* **Goal:** Plot constraints, solve the 2D LP graphically, and analyze objective slope sensitivity[cite: 1, 3].
* **Constraints:** $6x_1 + 3x_2 \ge 12$, $4x_1 + 8x_2 \ge 16$, $6x_1 + 5x_2 \le 30$, $6x_1 + 7x_2 \le 36$, $x_1, x_2 \ge 0$[cite: 2, 3].
* **Key Result:** Optimal solution at vertex **$(5, 0)$** with **$Z_{\max} = 15$** for $Z = 3x_1 + x_2$[cite: 7].

### **Exercise 2: Radiation Therapy Formulation & Minimization**
* **Goal:** Formulate an LP minimizing healthy tissue exposure subject to tumor target constraints[cite: 13].
* **Constraints:** $0.3x_1 + 0.1x_2 \le 2.7$, $0.5x_1 + 0.5x_2 = 6$, $0.6x_1 + 0.4x_2 \ge 12$ *(or equivalent bounds)*[cite: 13], $x_1, x_2 \ge 0$[cite: 13].
* **Key Result:** Optimal dose setting at vertex **$(7.5, 4.5)$** with **$Z_{\min} = 5.25$**.

### **Exercise 3: Animal Feed Blending Problem**
* **Goal:** Formulate a 12-variable LP model to minimize raw material procurement costs while satisfying nutritional requirements (Vitamins, Proteins, Calcium, Fat) across three feed types.

### **Exercise 4: Convexity Proofs**
* **Goal:** Analytical mathematical verification using the definition of convex sets ($\forall \lambda \in [0, 1]$):
  * $A = \{(x_1, x_2) \mid x_1^2 + x_2^2 \ge 3\}$: **Non-convex** (counterexample provided).
  * $B = \{(x_1, x_2, x_3) \mid x_1 + 2x_2 \le 1, x_1 - 2x_3 \le 2\}$: **Convex**.
  * $C = \{(x_1, x_2, x_3) \mid x_2 \ge x_1^2, x_1 + 2x_2 + x_3 \le 4\}$: **Convex**.
  * $D = \{(x_1, x_2, x_3) \mid x_3 = \vert{}x_2\vert{}, x_1 \le 3\}$: **Non-convex**.

### **Exercise 5: Hyperplanes & Basic Feasible Solutions**
* **Goal:** Identify $3D$ polyhedral vertices algebraically ($\binom{7}{3} = 35$ combinations), convert to standard form with slack variables, and compute Basic Feasible Solutions (BFS).
* **Key Result:** Optimal BFS found at **$(3.5, 6.5, 8.5)$** with **$Z_{\min} = 94.5$**.

### **Exercise 6: Simplex Method Implementation**
* **Goal:** Custom Python implementation of the Simplex tableau algorithm tracking entering/leaving variables and objective updates.
* **Key Result:** Converges to optimal solution **$(x_1, x_2, x_3) = (0.67, 0, 1.33)$** with **$Z_{\max} = 9.33$**.

---

## 🛠️ Tech Stack & Requirements

* **Language:** Python 3.x[cite: 1]
* **Core Libraries:**
  * `numpy` (System solving & matrix manipulation)[cite: 1]
  * `matplotlib` (Feasible region plotting & objective line sweeps)[cite: 1, 3]

---

## 📁 File Structure

```text
.
├── report.pdf               # Full academic report (University of Patras)
├── main.py                  # Consolidated Python scripts for Exercises 1-6
└── README.md                # Project documentation
