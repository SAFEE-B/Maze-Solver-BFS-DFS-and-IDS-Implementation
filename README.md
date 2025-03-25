# Maze Solver: BFS, DFS, and IDS Implementation

This project implements a **Maze Solver** using three search algorithms:

- **Breadth-First Search (BFS)**
- **Depth-First Search (DFS)**
- **Iterative Deepening Search (IDS)**

The goal is to navigate through a maze modeled as a graph from the **start node ("S")** to the **goal node ("I")**. Each room in the maze is represented by a unique vertex, and doors between rooms are represented by edges.

## 📊 Problem Overview
Given a maze with **11 rooms** and **15 connections**, the task is to find the path from the **entrance ("S")** to the **exit ("I")** using the three search algorithms.


### Graph Data Structure:
If given a Maze with rooms labeled as characters, we can model it into a graph as such.

graph = {
    'A': ['S'],
    'B': ['D', 'S', 'C'],
    'C': ['J', 'B'],
    'D': ['G', 'S', 'B'],
    'E': ['G', 'S'],
    'F': ['H', 'G'],
    'G': ['H', 'F', 'E', 'D'],
    'H': ['F', 'G', 'I'],
    'I': ['H', 'J'],
    'J': ['I', 'C'],
    'S': ['E', 'D', 'A', 'B']
}


## 📌 Algorithms Implemented

### 1. Breadth-First Search (BFS)
- Explores all neighbors at the current depth before moving deeper.
- Guarantees the shortest path.
- Suitable for shallow solutions.

### 2. Depth-First Search (DFS)
- Explores as far as possible along each branch before backtracking.
- May not find the shortest path.
- Can be more memory efficient than BFS but might get stuck in deep branches.

### 3. Iterative Deepening Search (IDS)
- Combines DFS and BFS by performing a depth-limited DFS repeatedly.
- Guarantees the shortest path.
- Space-efficient like DFS but optimal like BFS.

## 📂 Project Structure
```
├── UninformedSearchMaze.ipynb    # Jupyter Notebook with BFS, DFS, and IDS implementations
└── README.md                      # Project documentation
```

## 🧪 Requirements
Ensure Python is installed on your system. Recommended: Python 3.8+

### Install Jupyter Notebook (if not already installed):
```bash
pip install notebook
```

## ▶️ Usage

1. Clone the repository:
```bash
git clone https://github.com/SAFEE-B/Uninfomed-Maze-Search-BFS-DFS-IDFS-.git
cd Uninfomed-Maze-Search-BFS-DFS-IDFS-
```

2. Open the Jupyter Notebook:
```bash
jupyter notebook UninformedSearchMaze.ipynb
```

3. Run the notebook cells to execute BFS, DFS, and IDS algorithms.

## 📊 Performance Comparison

| Algorithm   | Completeness | Optimality | Time Complexity  | Space Complexity |
|-------------|--------------|------------|------------------|------------------|
| BFS         | ✅ Yes       | ✅ Yes     | O(V + E)         | O(V)             |
| DFS         | ✅ Yes       | ❌ No      | O(V + E)         | O(V)             |
| IDS         | ✅ Yes       | ✅ Yes     | O((V + E) * d)   | O(d)             |

- **V**: Number of vertices (rooms)
- **E**: Number of edges (doors)
- **d**: Depth of the goal node

## 📌 Key Insights
- **BFS** finds the shortest path but uses more memory.
- **DFS** is memory-efficient but may get stuck in deep paths.
- **IDS** balances both and finds the optimal path with less space usage.

## 🤝 Contributing
Feel free to fork this repository, make improvements, and submit a pull request!

## 🐜 License
This project is licensed under the MIT License.

