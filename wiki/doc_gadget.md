---
title: Gadget
tags: [analysis,data]
last_updated: November 3, 2015
summary: "Here you can find information relating to our core running code; Gadget."
---

## Parameters

For the simulation suite we use <span style="font-family:Courier">P-Gadget3</span> (first 24 halos) and <span style="font-family:Courier">Gadget4</span> (remainder). The parent directory of each folder contains `.gadget3` or `.gadget4` to indicate which halo was run with which code. We use the following compile flags for our runs. `PMGRID` changes depending on the resolution of the run. There is a great amount of documentation on each of these parameters on Phil Hopkin's [GIZMO website](http://www.tapir.caltech.edu/~phopkins/Site/GIZMO_files/gizmo_documentation.html).

```Text
PERIODIC  
UNEQUALSOFTENINGS  
PMGRID=512  
GRIDBOOST=2  
PLACEHIGHRESREGION=2  
ENLARGEREGION=1.2  
MULTIPLEDOMAINS=16  
PEANOHILBERT  
WALLCLOCK  
MYSORT  
DOUBLEPRECISION  
OUTPUT_IN_DOUBLEPRECISION  
INPUT_IN_DOUBLEPRECISION  
ORDER_SNAPSHOTS_BY_ID  
NO_ISEND_IRECV_IN_DOMAIN  
FIX_PATHSCALE_MPI_STATUS_IGNORE_BUG  
COMPUTE_POTENTIAL_ENERGY  
OUTPUTPOTENTIAL  
RECOMPUTE_POTENTIAL_ON_OUTPUT  
HAVE_HDF5  
DEBUG  
```

Parameter files for each of the runs can be found as `param.txt` in the relevant simulation directory. For those users who have access to `antares.mit.edu` (MKI's compute cluster), Brendan Griffen's home directory contains the master files (configuration files, parameter files and expansion factor lists for output) for the entire suite.

```bash
/home/bgriffen/exec/gadget3
/home/bgriffen/exec/gadget4
```