# Nonlinear Dynamics Homework

This repository contains two mini programs developed for a homework assignment on Nonlinear Dynamics. Each program explores a different chaotic map and demonstrates how simple iterative maps can lead to complex, chaotic behavior.

---

## Program 1: Standard Map Simulator

### Overview

This program simulates the **Standard (Chirikov) Map**, a classic area-preserving map used to study Hamiltonian chaos. The map is defined by the iterative equations:

- **\( y_{n+1} = \left( y_n - \frac{k}{2\pi}\sin(2\pi x_n) \right) \mod 1 \)**
- **\( x_{n+1} = (x_n + y_{n+1}) \mod 1 \)**

Here, \( x \) represents the phase (or angle) on a torus, and \( y \) represents a momentum-like variable. The parameter \( k \) controls the strength of the nonlinear perturbation. For small \( k \) the dynamics are regular (invariant tori), whereas larger \( k \) can induce chaotic behavior.

### How to Run

- The program iterates trajectories starting from a grid of initial conditions.
- Adjust parameters such as the number of iterations or the list of \( k \) values in the code.
- Run the program to generate phase-space portraits that illustrate the transition from order to chaos.

---

## Program 2: Chaos Map Explorer

### Overview

This program explores a custom chaotic map given by:

- **\( y_{n+1} = y_n - b\sin(2\pi x_n) \)**
- **\( x_{n+1} = \left( x_n + a\,(1 - y_n^2) \right) \mod 1 \)**

In this map:
- **\( x \)** is treated as an angular variable (confined to \([0,1)\) via the modulo operation).
- **\( y \)** is a momentum-like variable that is updated using a nonlinear (quadratic) function of \( y \) combined with a sinusoidal term in \( x \).

Changing the parameters \( a \) and \( b \) alters the dynamics:
- The parameter **\( a \)** affects the shift in \( x \) through the term \( a\,(1 - y^2) \).
- The parameter **\( b \)** modulates the sinusoidal kick on \( y \).  
By exploring different combinations of \( a \) and \( b \), you can observe a variety of phase-space structures from regular to chaotic motion.

This program also includes functionality to plot multiple parameter sets in a grid of subplots for side-by-side comparisons.

### How to Run

- Specify a range of values for \( a \) and \( b \) in the configuration.
- Run the program to generate subplots that display the phase-space portraits for each parameter pair.
- Use the zoom option to focus on specific regions of the phase space if desired.

---

## Dependencies

- **Python 3.x**
- **NumPy**
- **Matplotlib**

---

## Usage

1. **Clone or Download the Repository:**  
   Obtain the repository files to your local machine.

2. **Run the Programs:**  
   Open a terminal (or use an IDE) and navigate to the repository directory. Then run:
   ```bash
   python standard_map_simulator.py
   python chaos_map_explorer.py
