# VHDL Counter Overflow Bug

This repository demonstrates a potential overflow bug in a simple VHDL counter.  The counter is designed to count from 0 to 15, but if the clock frequency is too high, it might overflow and produce incorrect results. The `counter.vhdl` file contains the buggy code and `counter_fixed.vhdl` demonstrates a solution.

## Bug Description

The bug lies in the lack of robust handling of potential overflow conditions. If the clock's rising edge occurs too frequently, the counter could increment past its maximum value (15), leading to unexpected behavior or even simulation errors.

## Solution

The corrected code in `counter_fixed.vhdl` adds additional checks to prevent overflow. Although this example doesn't use a specific function to handle the potential overflow condition, it demonstrates the most common type of approach to prevent an integer from going out of bounds.