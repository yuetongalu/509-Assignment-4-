# 509-Assignment-4-
This repository is created for TECHIN 509 Assignment 4.

**1. Title and Description**
- Flood Fill defines criteria for determining whether a cell or pixel should be filled with the new value. Typically, this criterion is based on comparing the current cell's value with the value at the cellpoint. If they match, the cell is considered part of the region to be filled.
- In the context of a flood fill algorithm, "recursively fill adjacent cells" refers to the process of systematically visiting neighboring cells of the current cell (x, y) and applying the fill operation to them. This process is carried out recursively, meaning that the function calls itself to explore adjacent cells.
  
**2. Code Explanation**

**2.1 Flood Fill Function**
It takes the input board, old and new values, and the starting coordinates (x, y) as parameters. Its main role is to set up the initial conditions, create a copy of the input board (modified_board), and then call the nested fill function to perform the flood fill operation. Finally, it returns the modified board.

**2.2 Recursive Fill Adjacent Cells Function**
2.2.1 Start at a Cell: We begin at a specific cell, let's say (x, y), and check if it meets certain conditions for filling. These conditions could include checking if the cell's value is equal to a specific value (the "old" value).

2.2.2 Fill the Current Cell: If the conditions are met, we change the value of the current cell to the new value. This marks the current cell as part of the filled region.

2.2.3 Explore Adjacent Cells: After filling the current cell, we explore its adjacent cells. These are cells that are directly neighboring the current cell and can be in four directions: up, down, left, and right. For each adjacent cell, we perform the same filling process:

2.2.4 Check if the adjacent cell meets the fill conditions.
If it does, change the value of the adjacent cell to the new value.
Then, recursively call the fill function on the adjacent cell to explore its neighbors.

2.2.5 Recursion: The recursive calls continue the process, allowing us to explore deeper into the region. Each recursive call focuses on a different cell, and the process repeats until there are no more adjacent cells that meet the fill conditions or until the entire region is filled.
  

