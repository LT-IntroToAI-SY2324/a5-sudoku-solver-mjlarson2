# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

On the first puzzle, DFS and BFS went through the same number of iterations (58), but in the more difficult second puzzle
DFS went through 336 while BFS went through 555. This indicates that generally, DFS is more efficient, though it might suggest that
BFS could be more efficient in puzzles simpler than either of the two tested.


2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

The choice of data structures was fairly impactful on the implementation and functionality of those algorithms: the FIFO nature of the queue greatly helped facilitate the bread-first search, and the LIFO nature of the stack did the same for DFS. This same objective could likely have been done with conventional lists in some way, but the use of stack and queue feels like the easiest way to have done it.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

The sudoku solver might be adapted to other grid-based logic games by modifying the way the board is structured: a game like Picross, for example, only ever has two possibilities for a square, the correct one of which is determined by column and row rules, but the nature of BFS and DFS allows them to adapt to a different board structure as long as the board is designed with the rules of the game in-built in some way into each square. The lessons learned from this assignment are applicable to real-world problem-solving and optimization in how the efficiency of different methodologies is demonstrated with respect to scale: certain algorithms are more effiient than others based on the quantity or organization of the relevant data.
