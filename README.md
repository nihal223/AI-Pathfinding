# AI-Pathfinding
Shortest Path finding in a Grid world

Problem Statement:-
An agent operating in a grid-world has to quickly compute a path from the current cell it occupies to a target goal cell. Different cells in the grid have different costs for traversing them. For instance, some may correspond to impassable obstacles, others to flat and easy to traverse regions. There may also be passable but difficult to traverse regions (e.g., rocky, granular terrain or swamps) as well as regions that can accelerate the motion of a character (e.g., highways or navigable regions, etc.).

grid3.py generates the grid world
final_all.py runs Uniform cost search, A* and Wighted A* to compute the path


New algorithm:-
A* with sequential use of many heuristics

This approach aims to utilize information from many different heuristics, which are considered by running n + 1 searches in a rather sequential manner. Each search uses its own, separate priority queue. Therefore, in addition to the different h values, each state uses a different g value for each search. We use g0 to denote the g for an anchor search process, which must use an admissible/consistent heuristic for the overall process to return an optimal solution. We use g(i), (i = 1, 2, ..., n) for the other search procedures, which can make use of any type of heuristic including inadmissible ones.

The algorithm uses two variables in order to control how sub-optimal the overall, final solution will be. The first variable w1(≥ 1.0) is used to inflate the heuristic values for each of the search procedures, similar to Weighted-A* The second variable w1(≥ 1.0) is used as a factor to prioritize the inadmissible search processes over the anchor, admissible one. The algorithm runs the inadmissible search procedures in a round robin manner in a way, which guarantees that the solution cost will be within the sub-optimality bound w1w2 of the optimal solution cost.
