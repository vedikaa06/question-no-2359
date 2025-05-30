# question-no-2359
Solution to the question no 2359 on leet code 

2359. Find Closest Node to Given Two Nodes
You are given a directed graph of n nodes numbered from 0 to n - 1, where each node has at most one outgoing edge.

The graph is represented with a given 0-indexed array edges of size n, indicating that there is a directed edge from node i to node edges[i]. If there is no outgoing edge from i, then edges[i] == -1.

You are also given two integers node1 and node2.

Return the index of the node that can be reached from both node1 and node2, such that the maximum between the distance from node1 to that node, and from node2 to that node is minimized. If there are multiple answers, return the node with the smallest index, and if no possible answer exists, return -1.

Note that edges may contain cycles.

How it works
bfs function

Performs Breadth-First Search (BFS) from a starting node.

Fills the dist array with shortest distances from the start node to every other node in the graph.

The graph is represented as a one-way path (each node points to at most one neighbor via the edges array).

closestMeetingNode function

Runs bfs twice: once from node1 and once from node2, getting distances to all nodes.

Then, for each node, it checks:

If it’s reachable from both nodes.

Chooses the node where the maximum of the two distances is smallest.

Returns that node's index.
