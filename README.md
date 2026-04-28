# A4 DS351 — Tree and Graph Visualizations

**Course:** DS351 – Data Visualization  
**Semester:** Spring 2026  

---

## Datasets

### 1. Tree Dataset — Global Superstore (Kaggle)
**Source:** [Kaggle - Global Superstore Dataset](https://www.kaggle.com/datasets/apoorvaappz/global-super-store-dataset)

**Description:**  
The Global Superstore dataset contains retail sales data from a global superstore
operating across multiple markets and regions worldwide.

**Tree Structure:**
| Level | Represents |
|---|---|
| Root | World |
| Level 1 | Market (e.g., APAC, EU, US) |
| Level 2 | Region (e.g., Central Asia, Western Europe) |

**Nodes:** World, Markets, Regions  
**Edges:** Parent contains child (e.g., World → APAC → Central Asia)  
**Why ideal for Tree?** Strict parent-child hierarchy with one root node,
no cycles, and each region belongs to exactly one market.

---

### 2. Graph Dataset — Game of Thrones Battles (Kaggle)
**Source:** [Kaggle - Game of Thrones Dataset](https://www.kaggle.com/datasets/mylesoneill/game-of-thrones)

**Description:**  
This dataset contains records of all major battles from the Game of Thrones
universe, including which kings fought against each other.

**Graph Structure:**  
**Nodes:** Kings (e.g., Robb Stark, Joffrey/Tommen Baratheon, Stannis Baratheon)  
**Edges:** Two kings are connected if they fought a battle against each other  
**Weight:** Number of battles fought between the same two kings  
**Why ideal for Graph?** Has cycles, no hierarchy, no single root, and 
undirected weighted connections — a true general graph that cannot be 
represented as a tree.

---

## Visualizations

### Tree Layouts — Global Superstore

| Layout | Description | Link |
|---|---|---|
| Top-Down | Root at top, hierarchy flows downward level by level | [View](https://rayaan27.github.io/A4-DS351-Visualisations/tree_topdown.html) |
| Horizontal | Root on left, tree grows rightward | [View](https://rayaan27.github.io/A4-DS351-Visualisations/tree_horizontal.html) |
| Radial | Root at center, branches radiate outward in a circle | [View](https://rayaan27.github.io/A4-DS351-Visualisations/tree_radial.html) |
| Treemap | Nested rectangles sized by Sales value | [View](https://rayaan27.github.io/A4-DS351-Visualisations/tree_treemap.html) |

### Graph Layouts — GOT Battles Network

| Layout | Description | Link |
|---|---|---|
| Spring | Force-directed — connected kings cluster together naturally | [View](https://rayaan27.github.io/A4-DS351-Visualisations/graph_spring.html) |
| Circular | All kings evenly spaced on a circle, edges drawn across | [View](https://rayaan27.github.io/A4-DS351-Visualisations/graph_circular.html) |
| Spectral | Positions computed using graph eigenvectors | [View](https://rayaan27.github.io/A4-DS351-Visualisations/graph_spectral.html) |
| Kamada-Kawai | Force-directed using shortest-path distances | [View](https://rayaan27.github.io/A4-DS351-Visualisations/graph_kamada_kawai.html) |

---

## Libraries Used

- `pandas` — data loading and processing
- `networkx` — graph and tree construction
- `plotly` — interactive visualizations
- `numpy` — numerical computations

---

## How to Run

1. Clone this repository
2. Download the datasets from Kaggle links above
3. Place CSV files in the same folder as the notebook
4. Open `A4_2023xxx.ipynb` in VS Code or Jupyter
5. Run all cells in order
