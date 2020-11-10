# CRI
Determination of conservative and radical amino acid changes.


CRI v1.0

Usage:

In a unix terminal type:

    python cri.py input.txt

Where input.txt is a tab-delimited file with four columns. The four columns should be as follows:

    Branch#\tSite\tAncestral_amino_acid\tDerived_amino_acid

The input file should have a header line for each column.

The output file will have all the columns of the input file, plus conservative and radical calls for seven amino acid classification systems (see Sharbrough et al., 2018 Evolution, Table 1 for a description of the schemes) and a Conservative/Radical Index (CRI) score. The classification schemes are as follows:
    
    1) Zhang 2000 – Charge
    2) Zhang 2000 – Polarity 
    3) Zhang 2000 – Polarity and Volume
    4) Hanada et al. 2007 – Correlation with Ka/Ks
    5) Hanada et al. 2007 – Charge and Aromaticity
    6) Hanada et al. 2007 – Charge and Polarity
    7) Grantham 1974 – Charge and Hydrophobicity

Copyright Joel Sharbrough 2020. All rights reserved. This program is distributed under the MIT license, and can be used freely for any non-commercial efforts. If you use this program in your work, please cite the following papers:
    
    Sharbrough et al. 2018. Evolution. 72 (4), 808-824.
    Zhang. 2000. J Mol Evol. 50(1), 56-68.
    Hanada et al. 2007. Mol Biol Evol. 24(10), 2235-2241.
    Grantham. 1974. Science. 185 (4154), 862–864. 

Problems/suggestions should be addressed to Joel Sharbrough at joel.sharbrough [at] nmt.edu. An example input/output file is provided in the program package called "input.txt" and "output.txt".
