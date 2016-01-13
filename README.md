## biopython
Using the biopython module to find the distance between two atoms.
1/13: done by finding the distance between every atom in the molecule and then filtering by only the distances of the waters.

=======

###to run (in powershell/python): 
- make sure you are in the ```Python27``` folder and that the required ```.pdb``` files are in the same folder.  Mine are nested as ```Python27\biopython\filename```
- run ```python test.py```
- when prompted from input, type ```1FAT.pdb```

#####roadblocks:
* I'm not quite sure how to identify where waters are in the molecule (X)
* need to sort out how the hierarchy (Structure > Model > Chain > Residue > Atom) works (X)
* how to search within atoms when location is unknown
* how to isolate water as a residue -- waters are not a residue, they are listed in the same category as the R group. (X)
* how to use NumPy arrays. Is a matrix better in this case?


##### future things to include in the code:
* checks for proper file format
* ability to pull .pdb files from the database
* ability to preview which chain one is looking for



####9/24 eod:
use file 1FAT.pdb as detailed in <a href = "http://www.biotnet.org/sites/biotnet.org/files/documents/25/biopython_pdb.pdf" alt="the source"> this example source </a>. Will find distance between two atoms (everthing is hard coded at this point)

####10/6 eod:
altered code as in <a href ="http://stackoverflow.com/questions/26193034/can-any-one-help-me-understand-and-solve-this-error" alt="the source"> this stackoverflow article. </a> It will now calculate the distance between any two residue types in a structure.
However! It will not find waters (HOH) and it will also not calculate distance between two identical residue types. 

####11/18 eod:
asked Wes for help and we pseudo-coded how to fill a 2D array. will look into NumPy matrices since I think think could have benefits further down the line.

####10/27 eod:
the script will display the full id of any water molecule in the chain! The information is stored as a tuple, where the 'W' identifier signifies water. The next step would be to take those atoms and find the distance between them.

####113 eod:
Revisited this script, took a little bit of time to catch back up. Am thinking that storing all of the atoms in two arrays, then subtracting each entry and saving it in a 2D array. Then, filter by the waters. 
