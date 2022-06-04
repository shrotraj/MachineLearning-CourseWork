# Coursework: Solving Sudoku Puzzle

# Selection of algorithm

Given the coursework's problem statement. In most cases, the most obvious approach would have been to use a Naive Algorithm which uses linear search, but since the sudoku is a 9x9 matrix with 81 cells, each cell can be a number between 1 and 9, the different possible solutions add up to 9^81, which is an insanely large number that will eat up computational power and time with no guarantee of finding a viable solution.

To make sure we get a valid solution each time. I have selected the Backtracking alogirthm. Backtracking can be quick enough if it stays inside the restrictions and picks the right cells.


## What is Backtracking algorithm ?

Backtracking search is one of the methods of solving constraint networks. The generic backtracking algorithm was first described more than a century ago, and since then has been rediscovered many times [Bitner and Reingold, 1975]. For computer algorithms, backtracking is arguably the most fundamental Sudoku solution approach. It has the same meaning as the word. In certain cases, we may come to a dead end in our search for a solution and must return to the previous position to try again. For solving this sudoku puzzle i have used a recursive back tracking algorithm.

## Algorithm
The Algorithm starts with an assumption that we are provided with a incomplete sudoku puzzle board. This board can be a valid sudoku puzzle or a invalid one.
### Algoritm at high level:
- Step 1: Check if the given sudoku puzzle is valid or not.
- Step 2: 
  (i) If valid sudoku , Continue with Step 3.
  (ii) If Invalid sudoku, Replace all the cell element with -1.
- Step 3: Start iterating from the first first row to find a empty cell.
- Step 4: Try to place a number between (1-9) on that identified empty cell.
- Step 5: Check if the placed number is valid in the given spot on the curent board.
- Step 6: 
(i) If the placement is valid, Recursively try to place number in the board 		   using Step 1 - Step 3.
(ii) If the placement is not valid, reset the last inserted value and go back to previous step.
- Step 7: If all the empty cells are filled up return the final solved sudoku. 

### Overview of different code blocks:
#### Checking if sudoku is valid or not:
- Step 1: Check all the row for repeated digit, if found return False.
- Step 2: Check all the column for repeated digit, if found return False.
- Step 3: Check all the 3*3 matrix for repeated digit, , if found return False.
- Step 4: If all checks pass, return True.
#### Checking if number placement is valid or not:
This code block is implemented in the same principle as validation of sudko. But only difference is in this code block we are checking if the inserted number is not already present in the given row/column/3*3 code block.

## Code Performance in the given test set

Code was able to complete all 60/60 of the puzzles in the test set. However, code failed to complete some of the testcases under the hard puzzle category within the allowed duration of 20 seconds.


## References

[Bitner and Reingold, 1975] Bitner, J. R. and Reingold, E. M. (1975).  Backtrack programming techniques.  Communications of the ACM, 18(11):651–656.


