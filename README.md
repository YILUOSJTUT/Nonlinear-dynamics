# Nonlinear Dynamics Homework

This repository contains three mini programs developed for a homework assignment on Nonlinear Dynamics. Each program explores a different system that exhibits chaotic behavior, from discrete maps to continuous-time differential equations.

---

## Program 1: Standard Map Simulator

### Overview

This program simulates the **Standard (Chirikov) Map**, a classic area-preserving map used to study Hamiltonian chaos. The map is defined by the iterative equations:

- **\( y_{n+1} = \left( y_n - \frac{k}{2\pi}\sin(2\pi x_n) \right) \mod 1 \)**
- **\( x_{n+1} = (x_n + y_{n+1}) \mod 1 \)**

Here, \( x \) represents the phase (or angle) on a torus, and \( y \) represents a momentum-like variable. The parameter \( k \) controls the strength of the nonlinear perturbation. For small \( k \) the dynamics are regular (invariant tori), whereas larger \( k \) can induce chaotic behavior.

---

## Program 2: Chaos Map Explorer

### Overview

This program explores a custom chaotic map given by:

- **\( y_{n+1} = y_n - b\sin(2\pi x_n) \)**
- **\( x_{n+1} = \left( x_n + a\,(1 - y_n^2) \right) \mod 1 \)**

In this map:
- **\( x \)** is treated as an angular variable (confined to \([0,1)\)).
- **\( y \)** is a momentum-like variable updated by a nonlinear kick.

By varying parameters \( a \) and \( b \), users can observe transitions between regular and chaotic motion using side-by-side phase plots.

---

## Program 3: Driven Damped Pendulum (Chaos Simulator)

### Overview

The third program simulates the **driven damped pendulum**, a classic nonlinear system modeled by the second-order differential equation:

\[
\frac{d^2x}{dt^2} + a\frac{dx}{dt} + \sin(x) = f\cos(\omega t)
\]

Where:
- \( x \) is the angular displacement,
- \( a \) is a damping coefficient,
- \( f \) and \( \omega \) control the strength and frequency of the driving force.

We explore how varying these parameters leads to:
- Stable periodic motion
- Damped decay to rest
- **Chaotic dynamics** (sensitive dependence on initial conditions)

### Features

- Euler-based numerical integrator
- Modular code for reproducibility
- Visualization tools:
  - Time series plots
  - Phase space trajectories
  - Poincaré sections
  - Dot-style phase diagrams (for high-res chaos structure)

### Physics Insights

This simulation demonstrates how deterministic equations can produce unpredictable, aperiodic behavior. A small change in initial velocity or forcing amplitude results in diverging outcomes — the hallmark of **deterministic chaos**.



## Program 4: Nonlinear Wave Simulation (Coupled Oscillator Chain)

### Overview

This program simulates a **nonlinear 1D chain of coupled oscillators**, governed by a discretized second-order wave equation with both linear and cubic restoring forces:

\[
\frac{d^2P}{dt^2} = -\frac{1}{\rho} \left( \alpha P + \beta P^3 + k(2P - P_\text{left} - P_\text{right}) \right) + S(t)
\]

This setup can be interpreted physically as:
- Stress/strain waves in nonlinear elastic media
- Charge propagation in nonlinear transmission lines
- Toy models of seismic or mechanical wave transport

### Features

- Initialization with a **Gaussian wave packet**
- Optional **external sinusoidal source** at center
- Time evolution using **RK4 integrator**
- Visualizations:
  - Mean field \( \langle P(t) \rangle \) vs. time
  - Snapshot of wave profile at specific time steps

### Physics Insights

Without external forcing, the initial wave packet disperses and fades due to nonlinear dynamics and boundary reflections. With periodic forcing, energy can accumulate or create sustained wave structures depending on system parameters.

---

## Dependencies

- Python 3.x
- NumPy
- Matplotlib
- tqdm (for progress bars)

---

## Usage

```bash
# Clone the repository
git clone https://github.com/YILUOSJTUT/Nonlinear-dynamics.git

# Navigate to the folder
cd Nonlinear-dynamics

# Open notebooks in Jupyter
jupyter notebook
