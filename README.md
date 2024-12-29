# Bipartite-Matching

## Introduction
The ability to control light fixtures effectively in a building is crucial for ergonomic and architectural design. In this project, we address the challenge of determining whether switches can control lights while adhering to line-of-sight constraints imposed by walls in an L-shaped floor plan. The solution involves leveraging graph theory, particularly bipartite matching algorithms, to establish optimal switch-light pairings.
________________________________________
## Objective
The primary objective of this project is to:
1.	Develop a program that determines which switches can control which lights in a building with walls obstructing visibility.
2.	Ensure that the solution adheres to spatial constraints, including line-of-sight rules and wall obstructions.
3.	Provide a comprehensive output showing the maximum matching of switches to lights while adhering to all constraints.
________________________________________
## Problem Statement
In an L-shaped building:
•	There are n switches and n lights, each located at specific coordinates.
•	The building contains m walls, each defined by start and end points, which obstruct visibility between switches and lights.
•	A switch can only control a light if: 
1.	There is a direct line-of-sight between them.
2.	No wall intersects their line-of-sight.
3.	Both the switch and the light are in the same region (inside or outside the polygon formed by the walls).
The task is to determine the maximum number of switches that can control lights, ensuring that all constraints are satisfied.

________________________________________
## Solution
The solution uses a bipartite matching algorithm to assign switches to lights under the following steps:
### 1.	Input Representation:
-	Accepts user input for the number of switches, lights, and walls.
-	Coordinates for each switch, light, and wall segment are provided.
### 2.	Line-of-Sight Check:
-	Implements geometric calculations to verify: 
	If a switch and light are in the same region (inside or outside the polygon boundary).
	If any wall segment intersects the line connecting a switch and a light.
### 3.	Graph Construction:
-	Constructs a bipartite graph where edges connect switches to lights based on valid visibility.
### 4.	Maximum Matching:
-	Applies a depth-first search (DFS)-based bipartite matching algorithm to determine the optimal pairing of switches to lights.
### 5.	Output:
-	Displays the maximum number of switches that can control lights.
-	Specifies which switch controls which light.
-	Outputs a message if any switches or lights remain unmatched.

## Conclusion
This project successfully demonstrates the application of computational geometry and graph theory to solve a real-world problem. By using a bipartite matching algorithm with added constraints for line-of-sight and wall obstruction, the program ensures an optimal solution. This approach is not only efficient but also adaptable to more complex building layouts or additional constraints in future work.
