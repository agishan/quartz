Optimization is the process of determining the optimal solution to some problem, maximizing some objective whilst meeting all constraints.

Depending on the number of variables, constraints, computational power, and other factors, determining the optimal solution for a particular problem can be challenging. There are decision-making "heuristics" which can create solutions that are near-optimal in most situations. These heuristics can be thought of as:
- Algorithms that determine the order in which decisions are made
- Sets of rules that determine how decisions are made

If finding an optimal solution takes O(n!) time and we have 100,000 different possible variables, then solving it is infeasible.

We can group heuristics the same way we group operations research problems, such as Network, Scheduling, etc.

### Some Basic Heuristics Include:

#### 1. Nearest Neighbor Heuristic
- **Type of Problem**: Traveling Salesman Problem (TSP), Routing
- **How It Works**:
  - Start at an arbitrary node.
  - Repeatedly visit the nearest unvisited node until all nodes are visited.
  - Return to the starting node to complete the tour.
  - This heuristic is simple and provides a quick solution, but it does not guarantee the optimal tour.

#### 2. Kruskal’s Algorithm
- **Type of Problem**: Minimum Spanning Tree (MST), Network Design
- **How It Works**:
  - Sort all edges in the graph by their weight.
  - Add edges to the MST starting from the smallest, ensuring no cycles are formed.
  - Continue until the MST spans all vertices.
  - This heuristic finds the MST efficiently, which can then be used in various network optimization problems.

#### 3. Shortest Processing Time First (SPT)
- **Type of Problem**: Scheduling
- **How It Works**:
  - Order jobs by their processing times in ascending order.
  - Schedule jobs in this order.
  - This heuristic minimizes the average completion time of jobs but may not work well with constraints like deadlines.

#### 4. First Fit Decreasing (FFD)
- **Type of Problem**: Bin Packing
- **How It Works**:
  - Sort items in decreasing order of size.
  - Place each item in the first bin that has enough remaining space.
  - This heuristic provides a good approximation for the bin packing problem, though it may not always give the optimal number of bins.

#### 5. Greedy Algorithm
- **Type of Problem**: Various (Knapsack, Prim’s Algorithm for MST, Dijkstra’s Algorithm for Shortest Path)
- **How It Works**:
  - Make a sequence of choices, each of which is the best local option at the moment.
  - The heuristic builds up a solution piece by piece, always choosing the next piece that offers the most immediate benefit.
  - Greedy algorithms are easy to implement and can work well for many problems, but they do not guarantee global optimality.

### Example Heuristic Applications

#### Nearest Neighbor for TSP:
1. **Problem**: Given a set of cities and distances between each pair, find the shortest possible route that visits each city once and returns to the origin city.
2. **Heuristic**: Start at an arbitrary city, visit the nearest unvisited city, repeat until all cities are visited, then return to the start.

#### Kruskal’s Algorithm for MST:
1. **Problem**: Connect all nodes in a graph with the minimum total edge weight.
2. **Heuristic**: Sort edges by weight, add the smallest edge that doesn’t form a cycle, repeat until all nodes are connected.

#### Shortest Processing Time for Scheduling:
1. **Problem**: Minimize the total time to complete all jobs.
2. **Heuristic**: Sort jobs by their processing times and schedule them in that order.
