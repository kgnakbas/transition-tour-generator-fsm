# TT/CPT Generation for FSM

TT/CPT-Method for minimizing the length of $TT$ (Transition Tour) in the context of the Chinese Postman Problem (CPP). The goal is to find a minimum-cost tour that traverses every edge in a directed graph (digraph) at least once.

## Overview

When dealing with a strongly connected digraph $G(V, E)$ representing a Finite State Machine $FSM (M)$, the objective is to minimize the length of TT for $M$. This reduction can be achieved by finding a CPT of $G$.

### Symmetric Graphs

If $G$ is symmetric, the problem simplifies to finding an Euler tour of $G$. The condition for $G$ to contain an Euler tour is that it must be strongly connected and symmetric.

### Non-Symmetric Graphs

In cases where $G$ is not symmetric, every edge $\( e \in E \)$ must be included at least once, potentially more, in a minimal-cost tour. Finding a CPT of $G$ involves:

- Constructing a symmetric augmentation $G'$ of $G$, ensuring $G'$ is symmetric and strongly connected with minimal replicated edges.
- Finding an Euler tour of $G'$, which serves as a CPT for $G$.

## Example

```bash
# 
