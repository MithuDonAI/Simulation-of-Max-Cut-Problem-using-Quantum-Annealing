# Quantum Annealing for the Max-Cut Problem

**Author:** Kain Shivendrasingh  
**Roll Number:** 24B1817  
**Institute:** Indian Institute of Technology Bombay (IIT Bombay)

---

## Overview

This project implements **Quantum Annealing** to solve the **Max-Cut** combinatorial optimization problem. The Max-Cut problem, which is NP-hard, is mapped onto an **Ising Hamiltonian**, allowing the optimal graph partition to be obtained by finding the ground state of the corresponding quantum system.

The project simulates the **adiabatic quantum annealing** process using **PennyLane**, where the quantum system evolves from an easily prepared initial Hamiltonian to a problem Hamiltonian encoding the Max-Cut objective. The resulting solution is compared with the classical optimum to evaluate the effectiveness of the quantum approach.

---

## Objectives

- Understand the formulation of the Max-Cut problem.
- Map the optimization problem to an Ising Hamiltonian.
- Implement quantum annealing using PennyLane.
- Simulate adiabatic evolution of a quantum system.
- Extract the optimal cut from the final quantum state.
- Compare quantum and classical solutions.

---

## Background

### Max-Cut Problem

Given an undirected weighted graph

\[
G=(V,E),
\]

the objective is to partition the vertices into two disjoint sets such that the total weight of the edges crossing the partition is maximized.

The problem has applications in

- Network design
- VLSI circuit design
- Image segmentation
- Statistical physics
- Machine learning

---

### Quantum Annealing

Quantum annealing solves optimization problems by evolving a quantum system according to a time-dependent Hamiltonian

\[
H(s)=(1-s)H_B+sH_P,
\]

where

- \(H_B\) is the driver Hamiltonian
- \(H_P\) is the problem Hamiltonian
- \(s\in[0,1]\)

Initially the system is prepared in the ground state of \(H_B\). If the evolution is sufficiently slow, the **Adiabatic Theorem** guarantees that the system remains in its instantaneous ground state and finally reaches the ground state of \(H_P\), which corresponds to the optimal Max-Cut solution.

---

## Project Workflow

1. Define the graph.
2. Construct the corresponding Ising Hamiltonian.
3. Build the driver Hamiltonian.
4. Generate the time-dependent annealing Hamiltonian.
5. Simulate quantum evolution using PennyLane.
6. Measure the final quantum state.
7. Decode the bitstring into the graph partition.
8. Compare with the classical optimal solution.

---

## Features

- Quantum Annealing implementation using PennyLane
- Ising Hamiltonian construction
- Adiabatic time evolution simulation
- Ground-state energy estimation
- Max-Cut solution extraction
- Classical verification of results
- Visualization of graph partitions

---

## Technologies Used

- Python
- PennyLane
- NumPy
- NetworkX
- Matplotlib

---


## Results

The implementation successfully demonstrates how a combinatorial optimization problem can be reformulated as a quantum ground-state search problem. The annealing simulation converges toward the optimal graph partition for small graph instances, illustrating the principles of adiabatic quantum computation.

## References

1. Edward Farhi et al., *A Quantum Adiabatic Evolution Algorithm Applied to Random Instances of an NP-Complete Problem*, 2001.

2. Tameem Albash and Daniel A. Lidar, *Adiabatic Quantum Computation*, Reviews of Modern Physics, 2018.

3. PennyLane Documentation  
https://pennylane.ai

4. Lucas, A., *Ising Formulations of Many NP Problems*, Frontiers in Physics, 2014.

5. M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information*, Cambridge University Press.

---

## Author

**Kain Shivendrasingh**  
Roll Number: **24B1817**  
Engineering Physics  
Indian Institute of Technology Bombay
