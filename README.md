# Combinatorial Algorithms (Spring 2025)
## Assignment 1

**Authors:**  
- Hao Guo 
- Zirui Fang 

**Date:** April 2025  
**Course:** Combinatorial Algorithms  
**Instructor:** Prof. Pablo Ezequiel Terlisky  

---

## 📘 Overview
This repository contains our solutions for **Assignment 1** of the *Combinatorial Algorithms (104291)* course, Spring 2025.  
The assignment consists of two main programming exercises implemented in **Python**:

1. **Exercise 1:** Detecting *Induced Paw Subgraphs* in an undirected graph.  
2. **Exercise 2:** Computing the **Trotter–Johnson rank** of a valid topological permutation under given precedence constraints.

All source files are structured, documented, and can be executed in a Unix-based environment using Python 3.

---

## 🧩 Exercise 1 — Induced Paw Detection

### Description
A **paw graph** is a 4-vertex graph consisting of a triangle plus one additional vertex connected to exactly one vertex of the triangle.  

This program reads an undirected graph from standard input and outputs all **sets of 4 vertices** that form an **induced paw subgraph**, listed in **lexicographic order**.  
If no paw exists, it reports accordingly.

### Input Format
n m
v1 w1
v2 w2
...
vm wm
- `n`: number of vertices  
- `m`: number of edges  
- `vi wi`: edges between vertices (0-indexed)

### Output
- A list of vertex sets (each set as a list) forming induced paws, in lexicographic order.  
- If none found, prints: It found no paws in the graph.

### Example 1 (from assignment)
**Input**
7 10
1 2
1 3
2 3
3 4
2 4
0 1
0 4
6 4
5 3
2 6
**Output**
[0,1,2,3]
[0,2,3,4]
[0,2,4,6]
[1,2,3,5]
[1,2,3,6]
[1,2,4,6]
[2,3,4,5]

### Example 2 (no paws)
**Input**
6 12
0 1
0 3
1 3
2 1
2 4
4 1
5 3
5 4
3 4
0 2
0 5
2 5
**Output**
It found no paws in the graph.
### How It Works
1. Builds an **adjacency list** of the graph.  
2. Iterates over all **4-combinations of vertices** (without using `itertools`).  
3. For each combination:
   - Counts total edges between these 4 vertices.
   - Checks if they form a triangle + one pendant vertex.

ISSUES TO BE FIXED:

1. Assignment 1, Exercise 1, issue 1:
   Check if "continue" is allowed to be use!
2. Assignment 1, Exercise 2, issue 1:
   Both of ds_comb_ass_1-2.py and gpt_comb_ass_1-2.py have issues with printing the output after reading all the inputs. Fix it!!!

---


