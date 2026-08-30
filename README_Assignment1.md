

# Components in a Graph

## 📌 Problem Statement
There are \(2 \times N\) nodes in an undirected graph, with edges connecting nodes from the first half \([1, N]\) to the second half \([N+1, 2N]\).  
The task is to determine the size of the **smallest** and **largest** connected components that contain at least 2 nodes.  
Single isolated nodes should not be considered in the answer.

**Example Input:**
```
3
1 5
1 6
2 4
```

**Expected Output:**
```
2 3
```

---

# Approach
1. **Graph Representation**  
   - Build an adjacency list using a HashMap.  
   - Each node stores its neighbors.

2. **Traversal Method**  
   - Use **Breadth First Search (BFS)** to explore connected components.  
   - Maintain a `visited` set to avoid revisiting nodes.

3. **Component Size Calculation**  
   - For each unvisited node, run BFS to count the size of its component.  
   - Ignore components of size 1 (single nodes).  
   - Track the smallest and largest component sizes.

4. **Final Output**  
   - Print the smallest and largest component sizes separated by a space.

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
   <number_of_edges>
   <edge1_node1> <edge1_node2>
   <edge2_node1> <edge2_node2>
   ...
   ```

**Example Run:**
```
Input:
3
1 5
1 6
2 4

Output:
2 3
```

---


