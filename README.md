# qindia-qa101-final-project
The template for the final project of the QIndia quantum-algorithms-101 flipped classroom

## Task
The goal of this project is to implement a circuit that performs quantum amplitude estimation. You have the choice of doing this using Qiskit, Cirq or Braket.

The file u_init.py contains the function `u_init()` that will implement a circuit which performs the operation 

$$U_{init}|00\rangle = c_0|00\rangle + c_1|01\rangle + c_2|10\rangle + c_3|11\rangle$$

Implement the following functions in the language of your choice:
 1. `amplitude_estimation() -> float` which takes in the circuit generated by `u_init()` and finds the coefficient $c_2$ of the basis state $|10\rangle$ using the canonical amplitude estimation algorithm.
 2. `amplitude_estimation(basis: str) -> float` which can take in any basis state as an input ('00', '01', '10' or '11') and find the amplitude of that basis state