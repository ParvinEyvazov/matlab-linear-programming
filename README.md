# Knapsack and Maximum Stable Set problems with using Linear Programming in Matlab

This repository is about solving the most commonly known problems, knapsack, and maximum stable set using Linear Programming techniques in Matlab.

- [**Knapsack problem**](#1-knapsack-problem)
- [**Maximum Stable Set**](#2-maximum-stable-set)

## 1. Knapsack problem

The 0-1 Knapsack problem, which is, for a thief, to pick those items that have as much total value as possible while not exceeding the knapsack’s weight limit, using dynamic programming. In this question, firstly, you will formulate the 0-1 Knapsack problem as a combinatorial optimization formulation, a.k.a. binary integer programming formulation. Secondly, your goal is to solve the 0-1 Knapsack problem using the Simplex optimization algorithm instead of dynamic programming.

<br>

Typically, what we need to do is to convert the maximization formulation in https://en.wikipedia.org/wiki/Knapsack_problem into a minimization problem so that we can use the following Optimization Toolbox function https://www.mathworks.com/help/optim/ug/intlinprog.html which uses the Simplex algorithm to solve integer programming problems. Then, we will write our own Matlab function, which implements our minimization formulation of the 0-1 Knapsack problem, utilizing intlinprog. Our function header should be as “function x = knapsack(v,w,W)” where v and w are value and weight vectors
of the items, respectively, W is the weight capacity and x is a vector of indicator variables where xi=1 indicates that the i'th item has been put into the knapsack.

## 2. Maximum Stable Set

Matlab function to solve the Maximum Stable Set
problem explained in https://scipbook.readthedocs.io/en/latest/graph.html. Our function header should be as “function x = MSS(g)” where g is an nxn binary matrix where g(i,j)=1 if there is an edge between the i'th and j'th persons (i.e., they are unfriendly) and g(i,j)=0 otherwise and x is a vector of indicator variables where xi=1 indicates that the i'th person has been included in the picnic. We should use the intlinprog function.
