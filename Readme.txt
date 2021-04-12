The directory has 3 sub-folders:

1. stage_1 - creates initial equilibrated structure for a particular HEA alloy composition, in the family of Fe Ni Cr Co Cu 
2. tensile - example Lammps input script for performing uniaxial tensile deformation
3. compression - example Lammps input script for performing uniaxial compressive deformation

Some sample tasks - 
1. Decipher the strain rate used from the units
2. Perform mechanical deformation (tensile and compression), and study the
	Stress-strain response
	Deformation mechanisms (visualize in Ovito)
3. Effect of strain rate, temperature on deformation characteristics
4. Vary the alloying behavior, i.e., ternary to quarternary to quinary (5-element) and study the response. Here, you need to equilibrate each structure after choosing appropriate elements and their fractions (see "stage_1" folder). 
   To choose the compositions, please refer to the reference 'gorsse2018.pdf'
5. The deformation mechanisms may be correlated with the reference 'Meraj_2016.pdf' 
6. Structural characterization during deformation may be studied using the g(r) plots.

Note:
1. We are creating an FCC pure crystal containing 7 unit cells along each direction.
2. We use the Embedded atom Method (EAM) potential. 
3. To simulate 3 and 4-component alloys, you need to vary the lattice parameters accordingly, using a rule of mixtures approach. 
4. Use 6 processors for running the simulations. ystem to study both the elastic and plastic response. This may require a couple of trials to set the appropriate number of time steps in the simulation.
5. Output files:
  'deform.dump' contains positions, as well as several per-atom properties such as Potential and Kinetic energy and individual stress components. 
  'stress_strain.txt' contains the stress-strain data. Data is in 3 columns: column 1 - time step; 2 - strain and 3 - stress (in GPa). 