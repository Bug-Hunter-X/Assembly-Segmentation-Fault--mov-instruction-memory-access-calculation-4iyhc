# Assembly Segmentation Fault: mov instruction memory access calculation

This repository demonstrates a subtle bug in assembly code that can lead to a segmentation fault. The bug stems from an incorrect calculation in a `mov` instruction that accesses memory at an invalid address under specific runtime conditions.

## Bug Description
The `mov` instruction attempts to access memory using base register EBX, index register ESI, and a displacement.  An improper combination of values in EBX and ESI can push the memory address calculation out of bounds, resulting in a segmentation fault.

## Bug Reproduction
1. Assemble and link the `bug.asm` file.
2. Run the resulting executable.  The specific circumstances leading to the error might involve specific test data influencing EBX and ESI values.

## Solution
The `bugSolution.asm` file provides a corrected version of the code, addressing potential memory access issues through robust address validation or potentially using a different addressing method.

## Additional Notes
This bug highlights the importance of careful memory address calculation in assembly language programming and the need for thorough testing to uncover such subtle errors.