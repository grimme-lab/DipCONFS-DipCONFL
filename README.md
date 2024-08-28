# DipCONFS-DipCONFL
Geometries and electronic properties of the DipCONFS benchmark and DipCONFL data set. A detailed description is given in the [JCTC article](LINK). Both sets are separately available in xyz and HDF5 format.

## Structures of the HDF5 files
The HDF5 format contains one group per amino acid and dipeptide named according to the one-letter code. Each of these groups contains subgroups labeled by a number specifying the conformer.
For the DipCONFL, these subgroups include an attribute *number_of_atoms* with the total number of atoms *n* as well as the following data sets containing the properties of the conformer:

- *atomic_numbers*: Array of length *n* containing the atomic number of every atom.
- *coordinates*: Array of shape [*n*,3] containing the x, y, and z coordinates of every atom.
- *total_energy*: The total electronic energy of the conformer.
- *atomization_energy*: The atomization energy of the conformer.
- *gradients*: Array of shape [*n*,3] containing the gradients of every atom in x, y, and z direction.
- *dipole_moments*: Array of length 3 containing the dipole moment of the conformer in x, y, and z direction.
- *mulliken_partial_charges*: Array of length *n* containing the Mulliken partial charges of every atom.
- *hirshfeld_partial_charges*: Array of length *n* containing the Hirshfeld partial charges of every atom.

The DipCONFS HDF5 file is built up similarly but includes besides the structural information only the total electronic energies. All values are given in atomic units. Distances are in Bohr.
xyz files and sheets with the total electronic and conformational energies of the reference methods are additionally provided.
