# CRI
Determination of conservative and radical amino acid changes.


CRI v2.0

Usage:

In a unix terminal type:
    python2 CRI.py -f input.fasta > output.txt

Where input.fasta is a fasta file with amino acid alignments. Make sure 
alignments have the same length.

The output file will be tab-delimited, with the first column being the 1-based 
position from the alignment, the second column being the first amino acid, the 
third column being the second amino acid. After that, the conservative and 
radical calls for each of seven amino acid classification systems (see 
Sharbrough et al., 2018 Evolution, Table 1 for a description of the schemes) and 
a Conservative/Radical Index (CRI) score are given in successive columns. The 
classification schemes are as follows:

    1) Zhang 2000 – Charge
    2) Zhang 2000 – Polarity 
    3) Zhang 2000 – Polarity and Volume
    4) Hanada et al. 2007 – Correlation with Ka/Ks
    5) Hanada et al. 2007 – Charge and Aromaticity
    6) Hanada et al. 2007 – Charge and Polarity
    7) Grantham 1974 – Charge and Hydrophobicity

Finally, the character state for each sequence included in the alignment will be 
described in the remaining columns (in order of the sequences listed in the 
input fasta). Sites with >2 amino acids will be noted in the output file. CRI 
scores for those amino acid changes can be determined using the AA function for 
all pairwise combinations of amino acids as follows:
    
    python2 CRI.py -aa AA1 AA2

The output will be 10 columns in length, the first column, AA1, the second 
column AA2, columns 3-9 the conservative/radical calls for each of the amino 
acid classification schemes written above, and column 10 the CRI score. I have 
generated this for all amino acids and can be seen in AA_criScores.txt

Copyright Joel Sharbrough 2020. All rights reserved. This program is distributed 
under the MIT license, and can be used freely for any non-commercial efforts. If 
you use this program in your work, please cite the following papers:
    
Sharbrough et al. 2018. Evolution. 72 (4), 808-824 
Zhang. 2000. J Mol Evol. 50(1), 56-68.
Hanada et al. 2007. Mol Biol Evol. 24(10), 2235-2241.
Grantham. 1974. Science. 185 (4154), 862–864. 

Problems/suggestions should be addressed to Joel Sharbrough at 
joel.sharbrough [at] nmt.edu.
