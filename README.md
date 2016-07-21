#I-HEDGE
These are the two scripts that can be used in R to calculate the I-HEDGE metric, as described in: 

Jensen EL, Mooers A, Caccone A, Russello MA (2016) I-HEDGE: Determining the optimum complementary sets of taxa for conservation using evolutionary isolation. PeerJ

Two pieces of information are required to calculate I-HEDGE: a tree or splits-network depicting relationships among taxa, and a probability of extinction [p(ext)] for each taxon. 

I-HEDGE is calculated as follows. First, HED (heightened evolutionary distinctiveness)  values are used to calculate HEDGE, which is the product of HED and the p(ext) for the taxon (Steel et al. 2007). HEDGE is calculated initially for the entire set of taxa using the starting values of p(ext). The top-ranked taxon (eg., species X) is placed at the top of the I-HEDGE list. Next, assuming that species X will be “saved”, its extinction probability is then set to 0.001 and the HEDGE calculation is re-run. The top-ranked taxon from the second run that is not already prioritized was then given the overall second ranked position on the I-HEDGE list, its extinction probability is set to 0.001, and the procedure is repeated until all taxa have been prioritized.

References:

Steel M, Mimoto A, Mooers AO (2007) Hedging our bets: The expected contribution of species to future phylogenetic diversity. Evol Bioinform Online 3:237-244
