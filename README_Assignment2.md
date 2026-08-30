#rupeshnarayant
# Breadth First Search: Shortest Reach

## 📌 Problem Statement
You are given an undirected graph where each edge has a weight of **6 units**.  
For multiple queries, each query provides a list of edges and a starting node.  
The task is to determine the shortest distance from the starting node to all other nodes using **Breadth First Search (BFS)**.  

If a node is unreachable, return **-1** for that node.  
The output should exclude the starting node itself.

**Example Input:**
```
1
4 2
1 2
1 3
1
```

**Expected Output:**
```
6 6 -1
```

---

# Approach
1. **Graph Representation**  
   - Build an adjacency list for all nodes.  
   - Each node stores its neighbors.

2. **Initialization**  
   - Distances are initialized to `-1` (unreachable).  
   - The source node distance is set to `0`.

3. **Breadth First Search (BFS)**  
   - Use a queue to explore nodes level by level.  
   - For each edge, update distance as `dist[v] = dist[u] + 6`.

4. **Result Construction**  
   - Return distances for all nodes except the source.  
   - Print them in node order.

---

# How to Run
1. Save the code in a file named `Solution.java`.  
2. Compile the program:
   ```
   javac Solution.java
   ```
3. Run the program:
   ```
   java Solution
   ```
4. Provide input in the format:
   ```
   <number_of_queries>
   <n> <m>
   <edge1_node1> <edge1_node2>
   ...
   <edge_m_node1> <edge_m_node2>
   <start_node>
   ```

**Example Run:**
```
Input:
1
4 2
1 2
1 3
1

Output:
6 6 -1


