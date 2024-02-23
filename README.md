# Quantum Monte Carlo program
# Description
This FORTRAN 90 code is developed for the computation of the ground state energy of atomic and molecular systems using the Variational Monte Carlo and Pure Diffusion Monte Carlo methods.

The Variational Monte Carlo method employs a trial wave function that is iteratively optimized to minimize the expectation value of the Hamiltonian, providing an upper bound estimate of the ground state energy. Conversely, the Diffusion Monte Carlo method utilizes a stochastic algorithm to propagate a set of walkers in imaginary time, converging to the ground state wave function and yielding highly accurate estimates of the ground state energy.

The code contains the main program and all the subroutines needed for the energy calculation.

# System Requirements
- Fortran 90 Compiler
- Standard Fortran libraries

# Folder Structure
1. Input file `input.dat`
2. Main program `main.f90`
3. Output file `output.dat` generated after the execution of the program

# Installation
1. Clone the repository or download the source code
2. Compile the program using the Fortran 90 compiler
   ```
   gfortran main.f90 -o main

3. Execute the program 
   ```
   ./main

  # Usage
  1. Insert the parameters of the simulation in the input file, following the example ginven in `input.dat` file
  2. Compile and execute the program, as explained in Installation section
  3. The program will initiate the VMC and DMC calculations, providing in the output file the ground state energy estimate.

# Licence
This program is released under the GPL-3.0 Licence.

# Contact
For inquiries, bug reports, or suggestions, please reach out to martina.colucci@studenti.unipg.it
   
