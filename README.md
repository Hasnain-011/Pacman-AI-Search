# Pacman-AI-Search

## Project Overview
**Pacman-AI-Search** is an Artificial Intelligence project that implements and evaluates classical search algorithms to guide Pacman through maze-based environments. The goal is to analyze how different search strategies perform in terms of path optimality, speed, and exploration efficiency.

This project was developed as part of an academic AI assignment to demonstrate both uninformed and informed search techniques.

---

## Implemented Search Algorithms
The following algorithms are implemented and compared:

- **Depth-First Search (DFS)**
- **Breadth-First Search (BFS)**
- **Greedy Best-First Search (GBFS)**
- **A\* Search**

---

## Maze Environments
The algorithms are tested on three maze configurations to observe behavioral differences:

- **Tiny Maze** – Simple layout for basic comparison  
- **Medium Maze** – Moderate complexity  
- **Big Maze** – Complex environment to evaluate scalability  

---

## Experimental Results

### Tiny Maze
| Algorithm | Path Length | Nodes Expanded | Optimal |
|---------|------------|----------------|---------|
| DFS | 4 | 5 | Yes |
| BFS | 4 | 8 | Yes |
| GBFS | 4 | 5 | Yes |
| A* | 4 | 8 | Yes |

---

### Medium Maze
| Algorithm | Path Length | Nodes Expanded | Optimal |
|---------|------------|----------------|---------|
| DFS | 18 | 31 | Yes (by chance) |
| BFS | 18 | 31 | Yes |
| GBFS | 18 | 19 | Yes |
| A* | 18 | 57 | Yes |

---

### Big Maze
| Algorithm | Path Length | Nodes Expanded | Optimal |
|---------|------------|----------------|---------|
| DFS | 17 | 24 | No |
| BFS | 17 | 47 | Yes |
| GBFS | 17 | 18 | Yes |
| A* | 17 | 18 | Yes |

---

## Analysis & Observations
- **DFS** explores deeply and may find solutions quickly, but it does not guarantee optimal paths.
- **BFS** always finds the shortest path in unweighted mazes but expands many nodes.
- **GBFS** is the fastest in most cases due to heuristic guidance but may sacrifice optimality.
- **A\*** consistently provides the best balance between efficiency and correctness.

---

## Best Algorithm
### **A\* Search**
A* is considered the best overall algorithm because it combines:
- **Accuracy:** Guaranteed optimal paths  
- **Efficiency:** Heuristic-driven exploration reduces unnecessary expansions  

This balance makes A* widely used in real-world applications such as navigation systems, robotics, and game AI.

---

## How to Run
Execute the following commands to test the algorithms on different mazes:

```bash
python pacman.py -l tinyMaze -p SearchAgent
python pacman.py -l mediumMaze -p SearchAgent
python pacman.py -l bigMaze -z .5 -p SearchAgent
