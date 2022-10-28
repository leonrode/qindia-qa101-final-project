# qindia-qa101-final-project
The template for the final project of the QIndia quantum-algorithms-101 flipped classroom. Please fork this project before starting to work on it so that a repo get created in your own personal Github and you can have it as your own project!

## Setup
The goal of this project is to implement a circuit that performs quantum amplitude estimation. You have the choice of doing this using Qiskit, Cirq or Braket.

The file u_init.py contains the function `u_init()` that will implement a circuit which performs the operation 

$$U_{init}|00\rangle = c_0|00\rangle + c_1|01\rangle + c_2|10\rangle + c_3|11\rangle$$

To see if this works, open an IPython notebook in the repo and run the following

```
from u_init import u_init

qc = u_init('qiskit')
print(qc)
```

and you should see an image of the circuit. You can replace `qiskit` with your language of preference.

## Task
Implement the following functions (with however many helper functions you want) in the language of your choice:
 1. `amplitude_estimation() -> float` which takes in the circuit generated by `u_init()` and finds the coefficient $c_2$ of the basis state $|10\rangle$ using the canonical amplitude estimation algorithm.
 2. `amplitude_estimation(basis: str) -> float` which can take in any basis state as an input ('00', '01', '10' or '11') and find the amplitude of that basis state

You can add/change/remove any of the original files. Check that your circuit works using a simulator and that it gives the correct answers. Try and document your code as well as possible, including the precision of your algorithm.

## Tips & Tricks

Feeling a bit stuck? Then go over the worksheets and coding exercises for amplitude amplification, phase estimation and amplitude estimation. That should already get you quite far through the process. And of course don't hesitate to contact us, the instructors!

## Extensions
Once you have implemented the above tasks, feel free to add any extensions to the project you wish. Here are some suggestions below:

### Running on Quantum Hardware
 1. Run the algorithm on a real quantum hardware backend.
 2. Compare the performance of the algorithm on different real hardware backends.
 3. Improve the performance of the algorithm on real hardware by implementing error mitigation.

### Quantum Software extensions
 1. Program it in a way that the user can create the amplitude estimation circuit in any of the 3 languages.
 2. Include unit tests to check that your functions work as expected for different use cases.

### Quantum Algorithms extensions
 1. Allow the user to input the desired uncertainty
 2. Let the function take in custom $U_{init}$ circuits with more than 2 qubits
 3. Allow the user to input any combination of input states e.g. '00' and '01'.  
 4. Implement a non-canonical amplitude estimation algorithm, e.g. [Maximum Likelihood Amplitude Estimation](https://link.springer.com/article/10.1007/s11128-019-2565-2), [Iterative Amplitude Estimation](https://www.nature.com/articles/s41534-021-00379-1), [Power Law Amplitude Estimation](https://arxiv.org/abs/2012.03348) or [QoPrime Amplitude Estimation](https://arxiv.org/abs/2012.03348).
