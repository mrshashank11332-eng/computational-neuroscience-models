## computational-neuroscience-models
I used basic tools of python to analyze various neuronal models and mechanisms of neurons.


[![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive collection of foundational computational neuroscience and non-linear dynamical systems models built entirely from scratch in Python. This repository utilizes core control structures (`for` loops) and standard numerical libraries (`numpy`, `matplotlib`) to simulate neuronal excitability, ionic channel kinetics, and bifurcation theory without relying on high-level solver black boxes.

---

## Contents & Models Implemented

The repository is structured as an incremental progression through single-cell modeling, moving from basic integrate-and-fire mechanisms up to complex non-linear phase-space analysis:

# 1. Leaky Integrate-and-Fire (LIF) Model
* **Single Neuron Under Constant Current:** Simulates sub-threshold membrane potential dynamics and spike-reset behavior using explicit Euler integration under a constant applied current.

* **Two-Neuron Synaptic Network:** Extends the LIF framework to a coupled system where firing in a pre-synaptic neuron triggers a dynamic post-synaptic potential change via a simple synaptic weight addition.

# 2. Hodgkin-Huxley (HH) Ionic Gating Dynamics
* **Gating Variables vs. Voltage:** Evaluates activation (m, n) and inactivation (h) gating variables as functions of membrane voltage using standard rate equations.

* **Time Constants (tau_x vs. Voltage):** Computes and plots voltage-dependent kinetic time constants for channel opening and closing.

* **Potassium Channel Conductance Dynamics:** Simulates the trajectory of potassium macroscopic conductance (g_k n^4) following current step applications.

* **Full HH Action Potential Engine:** A complete implementation of the 4-variable Hodgkin-Huxley equations capturing the biophysical generation of an action potential under constant current injection.

* **Integration of 2-neuron and synapsis analysis:** Extended the HH model to a coupled system where firing in a pre-synaptic neuron triggers a dynamic post-synaptic potential change via a synaptic input from where synaptic conductance follows exponential decay with time.

# 3. Spatial structure of neuron and compartmental model:
* **Passive cable:** Used the solution of cable equation (green function) to understood how voltage changes with space and time for a linear dendrite. 

* **Compartmental model:** Simulated two compartments on a passive cable which are connected by axial current and first compartment receiving the constant current. 


# 4. FitzHugh-Nagumo (FHN) Phase-Plane & Bifurcation Analysis
* **2D Phase-Plane Plotter:** Maps cubic nullclines (du=0, dw=0) and directional vector fields (`plt.quiver`) to visualize system flows and fixed points.

* **Time-Integration Trajectories:** Simulates voltage responses to current pulses.

* **Bifurcation Parameter Sweep:** Automates parameter sweeps across applied currents (I) with transient slicing (`volt[1500:]`) to map the rheobase threshold, tonic firing windows (limit cycles), and upper depolarization blocks.

---





##  Requirements & Usage

All models are self-contained within the Jupyter Notebook (`Neuroanalysis.ipynb`). To run the simulations locally:

```bash
# Clone the repository
git clone [https://github.com/mrshashank11332-eng/computational-neuroscience-models.git](https://github.com/mrshashank11332-eng/computational-neuroscience-models.git)

# Install dependencies if needed
pip install numpy matplotlib jupyter

# Launch Jupyter Notebook
jupyter notebook Neuroanalysis.ipynb
```
## Future Roadmap 
* **Dynamic Synapses:** Implementing alpha functions and exponential decay for realistic synaptic currents (I_syn).
   
* **Coupled E-I Networks:** Building small network architectures to study synchronization and rhythm generation.
  
## Author

**Shashank Verma**
**BS-MS Dual Degree Student | IISER Pune**
**Focus: Computational Neuroscience & Non-linear Dynamical Systems**




