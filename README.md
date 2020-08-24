This folder contains predicted RNA structures for small RNA motifs in the 5' UTR of the SARS-COV2 genome
The structures are obtained using atomistic MD simulations with an external force (Adiabatic Bias MD) that promotes the formation
of a user-definded secondary structure. The protocol is the following

1. Plain MD simulation at 340K initialized from an extended configuration.
2. Extract 10 different RNA conformations from the simulation at step 1.
3. Solvate and equilibrate the structures in a new box
4. Perform pulling simulations. For each initial configurations, ABMD simulations are performed with KAPPA=2 and KAPPA=5
5. Continue the plain MD simulations (with no external bias) from step 4.
6. Select all the frames in 5. that have successfully adopted the desired secondary structure
7. Perform a cluster analysis on such structures
8. Extract centroids 


####  SL1 ####
GGGUUUAUACCUUCCCAGGUAACAAACCC
((((((.(((((....)))))..))))))

#### SL2 - AU  ###
GGAUCaCUUGUuGAUCU
.(((((.....))))).

#### SL2 - CG  ###
GGAUCcCUUGUgGAUCU
.(((((.....))))).

#### SL2 - GC  ###
GGAUCgCUUGUcGAUCU
.(((((.....))))).

#### SL2 - UA  ###
GGAUCuCUUGUaGAUCU
.(((((.....))))).

### SL3 ###
GUUCUCUAAACGAAC
((((.......))))


#### SL5 LOOP ###
ACGGUUUCGUCCGU
((((......))))