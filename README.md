# Off-by-one Error in Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The error occurs because the loop condition incorrectly includes the index equal to the vector's size, leading to accessing an element beyond the valid range.

The `bug.cpp` file contains the code with the error. The `bugSolution.cpp` file shows the corrected code.

## How to Reproduce

1. Clone this repository.
2. Compile `bug.cpp` (e.g., using g++).
3. Run the executable. You'll see an error (likely a segmentation fault or unexpected output).
4. Compile and run `bugSolution.cpp`. This version correctly iterates through the vector.

## Explanation

The error stems from the loop condition `i <= vec.size()`.  Vector indices are zero-based, meaning a vector of size `n` has valid indices from 0 to `n-1`.  The corrected condition should be `i < vec.size()`.