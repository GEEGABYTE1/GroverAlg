# Grover's Algorithm Experiment

A Simple Grover's Algorithm Experiement with 4 oracles.

These Oracles include `|00> `, ` | 11 >`, `|01 >`, `|01 >`. 

The diffuser is in the state `|11 >` to flip the state after the computation in the original state of `|00 >`. 

# How the Algorithm Works 

Our first step is to create an equal superposition of every possible input to the oracle. If our qubits all start in the state `|0 >`, we can simply create a superposition by appling a `H-gate` to each qubit. We can call this a superposition state `|s >`. For two qubit states, similarly, we can craete the state `|s >` from the state `|00 >` by applying a H-gate to each qubit. Moreover, since the H-gate is its own inverse, applying H-gates to each qubit also does `|s > -> |11 > `. 

Run the oracle circuit (`U_oracle`) on the inputted qubits. This is roughly proportional to the square root of the number of possible inputs.

Our last step is to create and call the diffuser. Essentially, the diffuser allows us to do a reflection around the state `|s >`. More specifically, this allows us to the rotation `|s > -> |11 >` with the cz gate.


Made by Jaival 🦖