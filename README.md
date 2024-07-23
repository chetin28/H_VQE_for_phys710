# H_VQE_for_phys710
 
Task 1

Compare the optimization convergence of the QNG Optimizer and the ~.pennylane.GradientDescentOptimizer for the simple single qubit VQE. Visualize the difference for at least 500 optimization steps

Task 2

Repeat the same comparison for Hydrogen VQE.

To construct our system Hamiltonian, we first read the molecular geometry from the external file. Create a file called "h2.xyz" with content

2 in Angstrom H 0.00000 0.00000 -0.35000 H 0.00000 0.00000 0.35000

using the ~.pennylane.qchem.read_structure function. The molecular Hamiltonian is then built using the ~.pennylane.qchem.molecular_hamiltonian function.

Task 3

Robustness in parameter initialization

While results above show a more rapid convergence for quantum natural gradients, what if we were just lucky, i.e., we started at a "good" point in parameter space? How do we know this will be the case with high probability regardless of the parameter initialization?

Using the same system Hamiltonian, ansatz, and device, try 10 independent trials with random parameter initializations.
