# 🚦 Quantum Traffic Light System

## Overview

The **Quantum Traffic Light System** is a quantum-inspired adaptive traffic signal controller that applies fundamental concepts from quantum computing—such as **superposition**, **probabilistic measurement**, and **feedback-based adaptation**—to simulate intelligent traffic control at a **three-way intersection**.

Unlike conventional traffic light systems that rely on fixed timings or deterministic logic, this model uses **probabilistic decision-making** to dynamically assign green-light durations based on evolving traffic conditions. The system is implemented using **IBM Qiskit** and evaluated through simulation on the **Qiskit Aer Simulator**.

---

## Motivation

Traditional traffic signal controllers often operate on static cycles or predefined rules, leading to inefficiencies when traffic distribution is uneven. Although classical adaptive systems exist, they usually require:

- Expensive sensing infrastructure  
- Continuous real-time optimization  
- Large datasets or pre-trained models  

This project explores a **quantum-inspired alternative** that:

- Introduces **controlled randomness** to avoid deterministic lock-in  
- Adapts automatically using **feedback**, not explicit optimization  
- Requires **no external dataset or pre-training**  
- Is **lightweight** and extensible to future quantum hardware  

---

## Core Idea

A **three-way intersection** is modeled using a **two-qubit quantum system**, producing four computational basis states:

| Quantum State | Interpretation |
|--------------|----------------|
| `|00⟩` | Road A receives the green signal |
| `|01⟩` | Road B receives the green signal |
| `|10⟩` | Road C receives the green signal |
| `|11⟩` | RESET (all-red safety interlock) |

Quantum circuits are constructed to place the system in **superposition** or to **bias probabilities** toward specific roads using rotation gates. Repeated measurements generate a probability distribution, which is converted into **green-light durations**.

An **adaptive controller** updates circuit parameters over time based on observed outcomes.

---

## Key Concepts Used

- Quantum superposition for unbiased signal selection  
- `RY` rotation gates to model traffic congestion bias  
- Probabilistic measurement as a decision mechanism  
- Shannon entropy to quantify uncertainty and learning  
- KL divergence to measure deviation from fairness  
- Feedback-based adaptive control  
- Safety interlock using a RESET state  

---

## Implementation Details

### Technology Stack

- **Programming Language:** Python  
- **Quantum Framework:** Qiskit  
- **Simulator:** Qiskit AerSimulator  
- **Numerical Computation:** NumPy  
- **Visualization:** Matplotlib  

### Core Components

- Quantum circuit construction (superposition & biased circuits)  
- Circuit execution and probability extraction  
- Mapping probabilities to green-light durations  
- Adaptive feedback loop for parameter updates  
- Visualization of probability evolution, entropy, and signal timing  
- Export of experiment history to **JSON** and **CSV** formats  

---

## Experimental Scenarios

### 1. Equal Superposition (Baseline)
- All roads receive nearly equal probability
- Validates fairness and unbiased behavior

### 2. Biased Traffic Condition
- Increased rotation bias simulates congestion on a specific road
- The congested road receives longer green duration

### 3. Adaptive Learning Over Time
- Controller updates parameters iteratively
- Converges toward busier roads while preventing starvation

---

## Results Summary

- Fair behavior under balanced traffic conditions  
- Successful prioritization of congested roads  
- Entropy decreases over time, indicating learning and stabilization  
- Controlled randomness prevents deterministic cycling  

---

## How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/sachhu04/Quantum-Computing-Course-Project.git
```

### 2. Open the Notebook
Open the Jupyter notebook in **Google Colab** or a local Jupyter environment.

### 3. Install Dependencies
```bash
pip install qiskit qiskit-aer numpy matplotlib
```

### 4. Run the Notebook
Execute the notebook cells sequentially.

---

## Limitations

- Uses **simulated quantum hardware**, not real quantum devices  
- Does not integrate **real-time IoT traffic sensor data**  
- Designed for a **single intersection**  
- Demonstrates a **quantum-inspired approach**, not a proven quantum speedup  

---

## Future Work

- Integration with real traffic sensor data (IoT-based systems)  
- Extension to **multi-intersection** traffic networks  
- Execution on **real IBM Quantum hardware** with noise analysis  
- Hybrid **quantum–classical optimization** strategies  
- Support for pedestrians, emergency vehicles, and priority lanes  

---

## Author

**Sachin**  
B.Tech Computer Science  
Indian Institute of Information Technology Kottayam  

⭐ If you find this project interesting, feel free to star the repository!# Quantum-Computing-Course-Project# Quantum-Computing-Course-Project
