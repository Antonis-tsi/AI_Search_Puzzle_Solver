# AI Puzzle Solver (UCS & A*)

A Java implementation of Artificial Intelligence search algorithms (Uniform Cost Search and A* Search) to solve a 1D sliding tile puzzle.

## The Puzzle
The game consists of a 1D board with 7 positions. The initial state contains 3 Black tiles ('B'), 3 White tiles ('W'), and 1 Empty space ('S').
Tiles can move into the empty space from adjacent positions (up to 3 steps away). The cost of each move is absolute to the distance traveled.

The goal is to reach a state where the specific alignment of tiles evaluates to a target score (sum = 30), effectively separating the tile types.

## Algorithms Implemented
* **Uniform Cost Search (UCS):** Explores nodes based on the lowest cumulative path cost.
* **A* Search (Astar):** Optimizes the search by combining the path cost and a heuristic function. The heuristic evaluates the current positions of the 'W' tiles to guide the search towards the goal state more efficiently.

## Project Structure
* `Main.java`: The entry point that runs both UCS and A* solutions sequentially.
* `GAME.java`: Defines the puzzle rules, state evaluation (`isGoal`), board representation, and valid move generation.
* `Node.java`: Represents a node in the search tree, tracking cost, depth, parent, and current state.
* `UCS.java` & `Astar.java`: The core search algorithm implementations utilizing Priority Queues for frontier management.


## Output
Upon execution, the program outputs the total number of explored nodes, the final cost, and the step-by-step solution path from the initial state to the goal for both algorithms.

## License
MIT License
