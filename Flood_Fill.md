**#Given board**
board = [
    "......................",
    "......##########......",
    "......#........#......",
    "......#........#......",
    "......#........#####..",
    "....###............#..",
    "....#............###..",
    "....##############....",
]

**#check the number of (x,y)**
#x= row, y = column (start from 0)
len(board) #number of x (row)

len(board[0]) #number of y (column)

**#flood fill function**
def flood_fill(input_board, old, new, x, y):
    modified_board = [list(row) for row in input_board]

   ** # Fill function**
    def fill(x, y):
        # (x,y) requirements
        if (
            x < 0
            or x >= 8
            or y < 0
            or y >= 22
            or modified_board[x][y] != old
        ):
            return  'wrong value'

       ** # Modify the cell**
        modified_board[x][y] = new

       ** # Recursively fill adjacent cells**
        fill(x + 1, y)
        fill(x - 1, y)
        fill(x, y + 1)
        fill(x, y - 1)

    # Start the flood fill from the initial position (x, y)
    fill(x, y)

    return modified_board

# Your board data
board = [
    "......................",
    "......##########......",
    "......#........#......",
    "......#........#......",
    "......#........#####..",
    "....###............#..",
    "....#............###..",
    "....##############....",
]

# Call the flood_fill function and get the modified board
modified_board = flood_fill(input_board=board, old=".", new="~", x=2, y=10)

# Print the modified board
for row in modified_board:
    print(''.join(row))



 modified_board = flood_fill(input_board=board, old=".", new="~", x=3, y=8)

# Print the modified board
for row in modified_board:
    print(''.join(row))

