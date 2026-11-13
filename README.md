# knapsack-exact-vs-genetic-algorithm
MATLAB group case study comparing an exact optimisation method and a Genetic Algorithm for the 0–1 Knapsack Problem, with solution-quality and runtime benchmarks.
# Exact Optimization vs. Genetic Algorithms for the 0–1 Knapsack Problem

A group case study for **Operational Research III (MFM 3142)**, Department of Mathematics, Faculty of Science, University of Ruhuna.

## Project overview

This study compares an exact optimization approach with a Genetic Algorithm (GA) for the 0–1 Knapsack Problem. It considers both solution quality and computation time, including a 20-item example and tests with larger problem sizes.

## Problem formulation

Given a set of items, each with a value (profit) and weight, choose items to maximize total value without exceeding the knapsack capacity. Each item is either selected or not selected:

\[
\max \sum_{i=1}^{n} p_i x_i
\quad\text{subject to}\quad
\sum_{i=1}^{n} w_i x_i \leq W,
\qquad x_i \in \{0,1\}.
\]

Here, \(p_i\) and \(w_i\) are the profit and weight of item \(i\), and \(W\) is the capacity.

## Methods

- **Exact optimization:** Used as the optimality benchmark in the study.
- **Genetic Algorithm:** A population-based heuristic that searches for high-value feasible item combinations. The report describes a population size of 50 for the 20-item example and 100 for the scalability experiments, with 100 generations, an 80% crossover rate, and a 10% mutation rate.

## Reported results

### 20-item example

| Method | Objective value | GA relative to exact |
|---|---:|---:|
| Exact method | 541 | 100% |
| Genetic Algorithm | 521 | 96.30% |

### Scalability experiments

| Number of items | Exact value | GA value | Exact time (s) | GA time (s) | GA relative to exact |
|---:|---:|---:|---:|---:|---:|
| 10 | 231 | 231 | <0.003 | 1.3021 | 100.00% |
| 50 | 1,570 | 1,430 | <0.003 | 1.2352 | 91.08% |
| 100 | 2,999 | 0 | <0.003 | 1.4163 | 0.00% |
| 150 | 4,616 | 0 | <0.003 | 1.4443 | 0.00% |
| 200 | 6,596 | 0 | <0.003 | 1.3551 | 0.00% |

The report’s GA returned a useful result for the smaller cases but failed to produce one in the 100-, 150-, and 200-item experiments. This highlights the importance of tuning the GA and handling capacity constraints carefully. Reported runtimes are specific to the study’s implementation and computing environment.

## Tools and topics

- MATLAB
- Operations research
- Integer optimization
- Combinatorial optimization
- Genetic algorithms
- Algorithm performance evaluation

## Code and reproduction

The report’s appendix refers to MATLAB code stored separately and does not specify source filenames or a run command. Add the relevant `.m` files to this repository and update this section with verified instructions before publishing the code.

## Project context

This was completed as a **group case study**. Add your individual contribution here if you want to describe your role—for example, model formulation, MATLAB implementation, result analysis, or report writing.
