# EzDSD

EzDSD is a software package for biologists to easily cluster 
biological networks using an integrated DSD ([diffusion state distance](https://doi.org/10.1371/annotation/343bf260-f6ff-48a2-93b2-3cc79af518a9))
and spectral clustering approach.

The clustering method used here is the winning method (K1) developed for 
the [DREAM](https://www.synapse.org/#!Synapse:syn6156761) challenge.

EzDSD offers the following features for network analysis:

* The ability to *easily* cluster groups of similar nodes
  to help mine important data about biological networks.
* To run the DSD on its own to retrieve either a similarity 
  or dissimilarity matrix describing the relationships between
  nodes. 

EzDSD also packages tools that score how significant 
these modules (clusters) are with respect to their association 
with complex traits and diseases. Of course, which 
traits/diseases are used is configurable.

It uses two different methods for this:

* The [FuncAssociate Service](http://llama.mshri.on.ca/funcassociate/) which 
  measures functional enrichment of a module.
* The [PASCAL](https://www2.unil.ch/cbg/index.php?title=Pascal) tool which
  scores modules using pathway analysis.

Both scoring tools have their benefits. FuncAssociate is orders of magnitude quicker 
to run and more easily configurable. PASCAL is the tool used in the DREAM challenge
and yields more nuanced information on the quality of clusters.

## Package Structure

The package is structured as follows:

```
EzDSD
|   README.md
|
|---Scoring
|   |
|   |---FuncAssociate
|   |   |   README.md
|   |   |   ...
|   |
|   |---PASCAL
|       |   README.md
|       |   ...
|
|---Clustering
|   |   README.md
|   |   ...
```

The top level directory contains installation, configuration
scripts, and documentation for the package as a whole. Lower
level directories contain the same with the appropriate level of granularity.
