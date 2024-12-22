# Stack Memory Deallocation Error in C
This repository demonstrates a common error in C: attempting to deallocate stack memory using `free()`. The `free()` function is only intended for memory allocated dynamically using functions like `malloc()`, `calloc()`, or `realloc()`.  Attempting to `free()` stack memory leads to undefined behavior, often resulting in program crashes or corruption.

The `bug.c` file contains the erroneous code. The `bugSolution.c` file demonstrates the corrected approach.

## How to Reproduce
1. Compile `bug.c`:
   `gcc bug.c -o bug`
2. Run the executable:
   `./bug`
3. Observe the behavior (likely a crash or unexpected output).

## Solution
The solution involves removing the `free(ptr)` call, as stack memory is automatically managed by the program. No explicit deallocation is needed.