# Tcl subtle type comparison bug
This repository demonstrates a subtle bug in a Tcl procedure related to type comparison. The `badproc` procedure incorrectly handles cases where the input values are of different types but represent the same numerical value.  The solution demonstrates how to handle type conversion for more robust comparisons.

## Bug Description
The original `badproc` procedure uses `==` to compare two values.  This operator performs a strict comparison, not handling implicit type conversion. As a result, if you compare "10" and 10 the result will be incorrect. 

## Solution
The improved solution demonstrates how to use the `expr` command for numerical comparison, handling implicit type conversion to achieve correct results even with different type input.