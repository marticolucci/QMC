# Quantum Monte Carlo program
# Description
This FORTRAN 90 code is developed for the computation of the ground state energy of atomic and molecular systems using the Variational Monte Carlo and Pure Diffusion Monte Carlo methods.

The Variational Monte Carlo method employs a trial wave function that is iteratively optimized to minimize the expectation value of the Hamiltonian, providing an upper bound estimate of the ground state energy. Conversely, the Diffusion Monte Carlo method utilizes a stochastic algorithm to propagate a set of walkers in imaginary time, converging to the ground state wave function and estimating the ground state energy.

The code contains the main program and all the subroutines and functions needed for the energy calculation. It has been developed for five specific cases: H atom, He atom, H2 molecule, H2+ ion and H3+ ion.

The user must specify in the input file the parameters of the simulation and the method that the programm will use for the calculation.

# System Requirements
- Fortran 90 Compiler
- Standard Fortran libraries

# Folder Structure
1. Input file `input.dat`
2. Main program `QMC.f90`
3. Output file `results.dat` generated after the execution of the program

# Installation
1. Clone the repository or download the source code
2. Compile the program using the Fortran 90 compiler
   ```
   gfortran QMC.f90 -o QMC

3. Execute the program 
   ```
   ./QMC

# Usage
  1. Insert the parameters of the simulation in the input file, following the example ginven in `input.dat` file
  2. Compile and execute the program, as explained in Installation section
  3. The program will initiate the VMC and DMC calculations, providing the output file containing the ground state energy and the acceptance ratio with the corresponding error.

# Input file Structure
The input file `input.dat` should be formatted as follows:

- Each parameter should be on a separate line.
- Comments can be included using the '!' character.

Below are the parameters expected in the input file and the name of the variables to which they are assigned:

- Method ('method'): specifies the method to be used for the simulation. Options include 'VMC' for Variational Monte Carlo or 'PDMC' for Pure Diffusion Monte Carlo.
- Number of electrons (n_e'): specifires the number of electrons in the system.
- Number of nuclei ('n_N'): specifies the number of nuclei in the system.
- System ('system'): indicates the system under consideration, for which the program will compute the ground state energy.
- a parameter ('a'): specifies the value of a parameter included in the definition of the wavefunction. It depends on the type of atom (eg. a=1 for H, a=2 for He).
- Time step ('dt'):
- Number of step at each simulation ('nmax'): speficies the maximum number of steps to be performed in each simulation.
- Reference energy ('E_ref'): Reference energy used in Diffusion Monte Carlo method to allow the convergence to the exact ground state.
- Imaginary time ('tau'): imaginary time introduced in Pure Diffusion Monte Carlo algorithm to facilitate the convergence towards the ground state wave function of the system.
- Number of Monte Carlo simulation ('nruns'): total number of MC simulations to be performed.

- Coordinates of the nuclei in the system: each line represents the coordinates of a single nucleus in the format x,y,z.

- Nuclear charges: each line represents the nuclear charge of a single nucleus. This parameter is needed in the calculation of the potential energy.

# Output file structure

The output file `results.dat` contains the results of the simulation. Below is a description of the information included in the output file:
- Information about the system, including:
  - the atom or molecule under consideration;
  - the number of electrons;
  - the number of nuclei;
  - coordinates of the nuclei;
- Method used to compute the energy;
- Results:
  - Estimated ground state energy with the corresponding error;
  - Acceptace ratio (ratio of number of accepted steps to total number of steps) with the corresponding error.

# Licence
This program is released under the GPL-3.0 Licence.

# Contact
For inquiries, bug reports, or suggestions, please reach out to martina.colucci@studenti.unipg.it
   
