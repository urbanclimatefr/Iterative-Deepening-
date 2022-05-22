# Iterative-Deepening

Implement the uninformed search algorithm iterative deepening for this problem. 

This problem is a graph search problem, and the graph search version of iterative deepening should be used.

- The problem statement is in problem_statement.pdf.

- Problem:
You work as an engineer for the entrepreneur Melon Husk in his business that makes
electric semi-autonomous cars. The eventual goal of the business is to create an entirely
autonomous vehicle that is able to drive itself from one place to another safely and avoid
traffic jams. Your task is one part of the overall goal: to find efficient routes through cities
that avoid traffic jams. Which algorithm should you use?
The prototype system will be tested in Manhattan. The streets of Manhattan are
famously laid out on a grid. Suppose we have a grid with 15 streets running North-South,
and 15 streets running East-West, as in the picture below. The distance between two
adjacent intersections is the same throughout the grid.

![image](https://user-images.githubusercontent.com/60503179/169689259-17285a6b-57cb-433a-ae49-d8a0bdc252f4.png)

- The file grids.txt contains five grids with different start and goal locations and traffic jams. The grids are represented as Java arrays filled with integers, where each integer represents one intersection. 0 means the intersection is clear, 1 represents a traffic jam, 2 represents the starting point, and 3 represents the goal.

- To implement iterative deepening, you will first need to represent a search node. A search node should contain three integers: the x and y location, and the depth of the node in the search tree. The x and y location are used to index into the grid arrays. For example, grid1[2][3]==2, so the first node when searching in grid1 should have x=2, y=3 and depth=0.

The implementation is in Java, and (assuming you’re using an object-oriented language) includes the following classes and methods:

A class called SearchNode with the following data and methods:
- The integers x, y, and depth, as described above. 
- A suitable constructor.
-	An equals method that compares the SearchNode with another object and returns true when they are of the same type and have the same state (the depth is not part of the state).
-	An expand method that creates the neighbours of the SearchNode. 
-	You may wish to implement the toString method (or the equivalent in your chosen language) to allow SearchNodes to be printed out conveniently. 

A class called IDSearch with the following methods:
-	A method called iterativeDeepening that contains the main loop of the iterative deepening algorithm (i.e. the loop that calls depthLimitedSearch repeatedly with increasing depth limits). 
-	A method called depthLimitedSearch that implements a depth-first graph search with a depth limit. 
-	A main method to start the program (or the equivalent in your chosen language). 

The depthLimitedSearch method will need data structures for the following:
-	The frontier;
-	All nodes generated within the current depth-first search (the explored set).
