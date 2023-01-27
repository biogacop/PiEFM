# Included notebooks

PiEFM.ipynb contains the main program to execute the PiEFM algorithm

To use it, you need the reduced stoichiometric matrix of a decoupled network (i.e. all reactions must be irreversible) and several other files containing:
- List of originally reversible and irreversible ones
- A dictionary that returns, for each originally reversible reaction, the index of its inverse in the decoupled model

PiEFM computes the EFMs and store them in a compressed format as frozensets of indices in the decoupled mode. If you prefer getting them as indices from the original model, you will also need another dictionary called toNonDecoupled

In order to get the decoupled model from an original one and all the associated files, you need the notebook decouplingModel.ipynb. These files must be put in the same directory that PiEFM.ipynb.

In its present state, both notebooks are prepared to work with the model 'e. coli core' that can be obtained from BIGGs

