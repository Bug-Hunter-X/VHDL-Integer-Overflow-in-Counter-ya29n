# VHDL Counter with Integer Overflow
This repository demonstrates a potential integer overflow issue in a simple VHDL counter and provides a corrected version.  The original code uses an integer type for the counter, which can lead to unexpected behavior if the count exceeds the maximum value.  The solution demonstrates using unsigned type to avoid this issue.

## Bug Description
The original `buggy_counter.vhd` uses an `integer` type for the counter. If the count reaches 15, it resets to 0. While functional, there could be a problem if the `integer` type were to be changed to a smaller range (i.e. 0 to 7) and the count exceeded its range, causing undefined behavior.

## Solution
The corrected code, `fixed_counter.vhd`, uses an `unsigned` type for the counter. This avoids the potential for integer overflow and provides more robust behavior.