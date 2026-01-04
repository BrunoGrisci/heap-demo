# heap-demo

<p align="right">
  <strong>English</strong> |
  <a href="README.pt-BR.md">Português (Brasil)</a>
</p>

A Python-based interactive demo of **min-heap data structures**.  
Includes **array and ASCII tree visualizations**, `heapify`, `insert`, `delete`, and `extract-min` operations, with optional **verbose step-by-step tracing** to illustrate how the **heap invariant** is maintained.

---

## 📌 Overview

> **Interactive Min-Heap Demo (CLI)**  
> Designed for teaching and learning **heaps and priority queues** in undergraduate algorithms and data structures courses.

This tool allows students to **see** how a min-heap evolves internally:
- how the array representation maps to a tree,
- how elements move during `sift-up` and `sift-down`,
- and why the heap property holds after each operation.

---

## 🖼️ Tool Overview (Visualization)

![Overview of the heap-demo](overview.png)

---

## 🎯 Main Goal

The primary goal of **heap-demo** is **pedagogical**:

- Make heap algorithms **transparent and observable**
- Bridge the gap between **array-based implementation** and **tree intuition**
- Support **step-by-step classroom demonstrations**
- Help students understand:
  - the **min-heap invariant**
  - parent/child index relationships
  - why `heapify` works bottom-up
  - how insertion and deletion preserve correctness

---

## 🧠 What This Tool Teaches

- Min-heap invariant: every node is ≤ its children
- Array representation of heaps (0-based indexing)
- Index relations:
  - `parent(i) = (i - 1) // 2`
  - `left(i) = 2i + 1`
  - `right(i) = 2i + 2`
- Core operations:
  - `heapify` (bottom-up)
  - `insert` / `push`
  - `extract-min` / `pop`
  - deletion at an arbitrary index
- Difference between **logical tree view** and **physical array storage**

---

## ⚙️ Implementation Overview

- **Language:** Python 3
- **Interface:** Interactive REPL (command-line)
- **Dependencies:** None required  
  - If `colorama` is installed, it is used automatically on Windows for colored output
- **Visualization:**
  - Array view with index:value pairs
  - ASCII tree rendered level by level
  - Optional blue-highlighted nodes and swaps
- **Tracing:**
  - Step-by-step execution with pauses (`verbose on`)
  - Explicit messages for swaps, checks, and termination conditions

---

## ▶️ How to Run

Clone the repository and run the script:

```bash
git clone https://github.com/BrunoGrisci/heap-demo.git
cd heap-demo
python3 heap_demo.py
```

The program starts an interactive shell:

```
Interactive Min-Heap Demo (with blue highlights)
Type 'help' to see commands. Values can be ints or any comparable types.
minheap>
```
---

## 🕹️ How to Use (REPL Commands)

Type `help` inside the tool to see all available commands.

### Core Commands

```
viz | visualize             Print the heap as array and ASCII tree
push X | insert X           Insert value X
pop | extractmin            Remove and print the minimum element
delete i | del i            Remove element at array index i
peek | findmin              Print the current minimum
len                         Print number of elements
clear                       Empty the heap
array                       Show only the underlying array
```

### Loading and Building Heaps

```
load [a,b,c,...]            Replace heap with given list, then heapify
heapify                     Re-heapify the current array
random N [lo hi]            Load N random integers (optional range)

```

### Tracing and Interaction

```
verbose on|off              Toggle step-by-step colored tracing
quit | exit                 Leave the program

```
---

## 🔍 Example Session

```
minheap> load [7,3,10,9,4,12,8,15,20,5]
minheap> viz
minheap> verbose on
minheap> push 2
minheap> pop

```

When `verbose` mode is enabled, the tool:

- highlights the indices involved in each operation,
- prints the reason for each swap or check,
- pauses between steps to allow discussion.

---

## ⚠️ Notes for Students

- The command `delete i` removes an element by array index, not by value.
- All values stored in the heap must be mutually comparable.
- This is a min-heap implementation (not a max-heap).
- The goal is understanding, not efficiency or large-scale use.

---

 🧑‍🏫 Suggested Classroom Uses

- Live demonstrations during lectures
- Guided laboratory sessions
- Comparing `heapify` vs repeated insertions
- Visualizing `sift-up` and `sift-down`
- Supporting discussions on correctness and invariants
- Debugging exercises (“Why does the algorithm stop here?”)

---

## 📖 References

- T. H. Cormen et al., Introduction to Algorithms, MIT Press
- J. Kleinberg & É. Tardos, Algorithm Design

---

## 👨‍🏫 Credits

**Author:**
Prof. Bruno Iochins Grisci
https://brunogrisci.github.io/

**Course:**
Projeto e Análise de Algoritmos I

**Institution:**
Universidade Federal do Rio Grande do Sul (UFRGS)
Instituto de Informática
Departamento de Informática Teórica

**Contributors:**
Bruno Iochins Grisci
Rodrigo Machado

---

## 📄 License

This project is licensed under the MIT License.
See the `LICENSE` file for details.

