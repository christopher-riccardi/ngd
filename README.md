*Normalized Google Distance*

To the best of my knowlegde, Choi and Rashid (2008, see citation file) first integrated the Normalized Google Distance (NGD) into protein sequence comparison. 

Given two amino acid sequences $X$ and $Y$, the NGD is calculated using the following formula:
```math
  NGD_{X,Y} = \frac{\max\left(\sum W_X, \sum W_Y\right) - \sum \min(W_X, W_Y)}{\left( \sum W_X + \sum W_Y \right) - \min \left( \sum W_X, \sum W_Y\right)}
```

where $\sum W_X$ and $\sum W_Y$ are the total $k$-mer counts of both sequences, respectively, $\sum \min(W_X, W_Y)$ is the sum of the $k$-mers common to both sequences, with the sum using whichever $k$-mer count is the lesser between the two sequences, $\max\left(\sum W_X, \sum W_Y\right)$ is the maximum and $\min \left( \sum W_X, \sum W_Y\right)$ is the minimum count between sequences $X$ and $Y$, respectively. This distance statistic is calculated to quantify the dissimilarity between two sequences based on their $k$-tuple compositions as it is derived from the Google similarity distance, used to find semantic similarity in web pages.

Usage:
```python
python ngd <fasta1> <fasta2> [optional, the k-mer size. Default=3]
```

I include three testing files s1, s2 and s3. s1 and s2 are more similar to each other than any is to s3.
