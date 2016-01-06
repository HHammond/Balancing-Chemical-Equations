# [2015-10-16] Challenge 236 [Hard] Balancing chemical equations
https://www.reddit.com/r/dailyprogrammer/comments/3oz82g/20151016_challenge_236_hard_balancing_chemical/

The program takes as input from STDIN a list of strings representing chemical
equations in standard form and returns strings of the balanced equations or
explaining that the equation couldn't be solved by this program. 

The solution is computed by converting the chemical equation into a homogeneous
linear system and computing an integer solution which belongs to the nullspace
of the system. 

Usage:

```
julia chem.jl < equations.txt
```

## Issues:

* There are valid equations which this program fails to balance (e.g. `(CuOH)2CO3 
  -> CuO + CO2 + H2O`).
* Sometimes it computes negative values (e.g. `U3O8 + HNO3
  -> UO2(NO3)2 + NO2 + H2O` maps to `U3O8 + -4HNO3 -> 3UO2(NO3)2 + -10NO2 + 
  -2H2O`) 
