# VHDL Counter Bug: Missing 'else' statement

This repository demonstrates a subtle bug in a VHDL counter implementation. The bug is related to a missing `else` statement in a conditional assignment within a clocked process. This leads to unexpected counter behavior.

## Bug Description
The provided VHDL code implements a simple 4-bit counter. However, the `if` statement within the clocked process lacks an `else` case. This means that if the counter reaches its maximum value (15), it resets correctly, but if it is not at its maximum value, it does nothing. Thus, in the next clock cycle, the count will not increment. This unexpected behavior can lead to design errors and incorrect functionality.

## Bug Solution
The solution involves adding the missing `else` statement to the conditional assignment. This ensures that the counter increments properly in every clock cycle, unless the reset signal is high.