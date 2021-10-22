# Sudoku-Generator
Generates Sudoku puzzles that have a unique solution. Able to generate either easy (requires nothing harder than hidden singles) puzzles, or medium/difficult puzzles (sometimes requiring extreme strategies/techniques like cell-forcing chains). The algorithm that generates difficult puzzles gives you not only unique boards, but boards where you cannot remove any more numbers without destroying the uniqueness of the solution.



Generator: The generator starts with an empty 9x9 grid and fills it up by iterating from the top left cell to the bottom right, 
and filling in the cells by trying random numbers. It checks if the inserted number works, and if so, continue on recursively.
 Then the full 9x9 grid is reduced down so that it becomes the start of a Sudoku puzzle. 
 It generates a list of integers 0-80 representing the indices in the puzzle, then scrambles the order. 
 To reduce, we try to remove the number at the first index in the list and then attempting to solve the puzzle. 
 If there exists more than one solution, then it is not a valid Sudoku puzzle, so undo the last change. 
 If easy puzzles are desired, then after a puzzle with a unique solution is found, algorithm stops.
  If difficult puzzles are wanted, then even after a valid puzzle is found, all the remaining indices are tried to see if the puzzle can be made any harder.
   The difficult puzzles are not only unique boards, but boards where you cannot remove any more numbers without destroying the uniqueness of the solution.
