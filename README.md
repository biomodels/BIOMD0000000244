# BIOMD0000000244: 

## Installation

Download this repository, and install with distutils

`python setup.py install`

Or, install using pip

`pip install git+https://github.com/biomodels/BIOMD0000000244.git`

To install a specific version (in this example, from the 2014-09-16 BioModels release)

`pip install git+https://github.com/biomodels/BIOMD0000000244.git@20140916`

## Usage

Importing the model package.

`import BIOMD0000000244 as model`

Get the SBML string from the model

`print model.sbmlString`

If [python-libsbml](https://pypi.python.org/pypi/python-libsbml) bindings are
installed, the libsbml.SBMLDocument object is also accessible

`model.sbml`


# Model Notes


This is the model described in: **Bacterial adaptation through distributed
sensing of metabolic fluxes**  
Oliver Kotte, Judith B Zaugg and Matthias Heinemann;_Mol Sys
Biol_2010;**6**:355.
doi:[10.1038/msb.2010.10](http://dx.doi.org/10.1038/msb.2010.10);  
**Abstract:**   
The recognition of carbon sources and the regulatory adjustments to recognized
changes are of particular importance for bacterial survival in fluctuating
environments. Despite a thorough knowledge base of Escherichia coli's central
metabolism and its regulation, fundamental aspects of the employed sensing and
regulatory adjustment mechanisms remain unclear. In this paper, using a
differential equation model that couples enzymatic and transcriptional
regulation of E. coli's central metabolism, we show that the interplay of
known interactions explains in molecular-level detail the system-wide
adjustments of metabolic operation between glycolytic and gluconeogenic carbon
sources. We show that these adaptations are enabled by an indirect recognition
of carbon sources through a mechanism we termed distributed sensing of
intracellular metabolic fluxes. This mechanism uses two general motifs to
establish flux-signaling metabolites, whose bindings to transcription factors
form flux sensors. As these sensors are embedded in global feedback loop
architectures, closed-loop self-regulation can emerge within metabolism itself
and therefore, metabolic operation may adapt itself autonomously (not
requiring upstream sensing and signaling) to fluctuating carbon sources.

In its current form this SBML model is parametrized for the glucose to acetate
transition and to simulate the extended diauxic shift as shown in figure 3 and
scenario 6 of the attached matlab file. In this scenario the cells first are
grown from an OD600 (BM) of 0.03 with a starting glucose concentration of 0.5
g/l for 8.15 h (29340 sec). Then a medium containing 5 g/l acetate is
inoculated with these cells to an OD600 of 0.03 and grown for another 19.7
hours (70920 sec). Finally the cells are shifted to a medium containing both
glucose and acetate at a concentration of 3 g/l with a starting OD600 of
0.0005.  
The shifts where implemented using events triggering at the times determined
by the parameters _shift1_ and _shift2_ (in hours). To simulate other
scenarios the initial conditions need to be changed as described in the
supplemental materials ([supplement
1](http://www.nature.com/msb/journal/v6/n1/extref/msb201010-s1.pdf))  
The original SBML model and the MATLAB file used for the calculations can be
down loaded as supplementary materials of the publication from the MSB
website. ([supplement
2](http://www.nature.com/msb/journal/v6/n1/extref/msb201010-s2.zip)).

The units of the external metabolites are in [g/l], those of the biomass in
optical density,OD600, taken as dimensionless, and [micromole/(gramm dry
weight)] for all intracellular metabolites. As the latter cannot be
implemented in SBML, it was chosen to be micromole only and the units of the
parameters are left mostly undefined.

This model originates from BioModels Database: A Database of Annotated
Published Models. It is copyright (c) 2005-2010 The BioModels Team.  
For more information see the [terms of
use](http://www.ebi.ac.uk/biomodels/legal.html).  
To cite BioModels Database, please use [Le Novère N., Bornstein B., Broicher
A., Courtot M., Donizelli M., Dharuri H., Li L., Sauro H., Schilstra M.,
Shapiro B., Snoep J.L., Hucka M. (2006) BioModels Database: A Free,
Centralized Database of Curated, Published, Quantitative Kinetic Models of
Biochemical and Cellular Systems Nucleic Acids Res., 34: D689-D691.](http://ww
w.pubmedcentral.nih.gov/articlerender.fcgi?tool=pubmed&pubmedid=16381960)


