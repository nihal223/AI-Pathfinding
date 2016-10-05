# AI-Pathfinding
Shortest Path finding in a Grid world

Problem Statement:-
An agent operating in a grid-world has to quickly compute a path from the current cell it occupies to a target goal cell. Different cells in the grid have different costs for traversing them. For instance, some may correspond to impassable obstacles, others to flat and easy to traverse regions. There may also be passable but difficult to traverse regions (e.g., rocky, granular terrain or swamps) as well as regions that can accelerate the motion of a character (e.g., highways or navigable regions, etc.).

grid3.py generates the grid world
final_all.py runs Uniform cost search, A* and Wighted A* to compute the path
