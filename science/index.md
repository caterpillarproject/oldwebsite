---
layout: static
title: Science
---

<b>Last Updated:</b> 22nd February, 2016.

## Papers

<ul class="projectlist">
<li>
  <a href="http://adsabs.harvard.edu/abs/2016arXiv161100759G">
      <img src="/assets/gallery/papers/paper4.png">
      <div class="container">
        <span class="projectlistheading">Tracing the first stars and galaxies of the Milky Way</span><br />
        Lead Author: Griffen, Brendan F. <br>
        Dooley, Gregory A.; Ji, Alexander P.; O'Shea, Brian W.; Gómez, Facundo A.; Frebel, Anna
      </div>
  </a>
  </li>
<li>
  <a href="http://adsabs.harvard.edu/abs/2016arXiv161000708D">
      <img src="/assets/gallery/papers/paper3.png">
      <div class="container">
        <span class="projectlistheading">An observer's guide to the (Local Group) dwarf galaxies: predictions for their own dwarf satellite populations</span><br />
        Lead Author: Dooley, Gregory A. <br>
        ; Peter, Annika H. G.; Yang, Tianyi; Willman, Beth; Griffen, Brendan F.; Frebel, Anna
      </div>
  </a>
  </li>
<li>
  <a href="http://adsabs.harvard.edu/abs/2016arXiv160909528C">
      <img src="/assets/gallery/papers/paper2.png">
      <div class="container">
        <span class="projectlistheading">JINA-NuGrid Galactic Chemical Evolution Pipeline</span><br />
        Lead Author: Côté, Benoit <br>
        Ritter, Christian; Herwig, Falk; O'Shea, Brian W.; Pignatari, Marco; Silvia, Devin; Jones, Samuel; Fryer, Chris L.
      </div>
  </a>
  </li>
  <li>
  <a href="http://adsabs.harvard.edu/cgi-bin/bib_query?arXiv:1509.01255">
      <img src="/assets/gallery/papers/paper1.png">
      <div class="container">
        <span class="projectlistheading">The Caterpillar Project: A Large Suite of Milky Way Sized Halos</span><br />
        Lead Author: Griffen, Brendan F. <br>
        Ji, Alexander P.; Dooley, Gregory A.; Gómez, Facundo A.; Vogelsberger, Mark; O'Shea, Brian W.; Frebel, Anna
      </div>
  </a>
  </li>
</ul>

## Cosmological Parameters
[Planck 2013 Cosmology](http://adsabs.harvard.edu/cgi-bin/bib_query?arXiv:1303.5076)

  \\(\Omega_{\Lambda}\\) | \\(\Omega_{m}\\) | \\(\sigma_{8}\\) | \\(n_{s}\\) | \\(h\\)
  :---: | :---: | :---: | :---: | :--:
  0.68  | 0.31  | 0.83  | 0.96  | 0.67

## Simulation Parameters

### Parent Simulation

  Volume <br> *h*^3 Mpc^3 | # particles | \\(m_{dm}\\) <br> 10^7 *h*^-1 \\(M_\odot\\) | \\(m_{dm}\\) <br> 10^7 \\(M_\odot\\) | \\(\epsilon_{dm}\\) <br> pc 
  :---: | :---: | :---: | :---: | :---: 
        100^3          | 1024^3 | 9 | 12 | 2441 

### Caterpillar (zoom-in) Simulations

~*Aquarius* <br> Level | MUSIC <br> *levelmax* | Effective <br> Resolution | \\(m_{dm}\\) <br> 10^4 *h*^-1 \\(M_\odot\\) | \\(m_{dm}\\) <br> 10^4 \\(M_\odot\\) | \\(\epsilon_{dm}\\) <br> pc 
  :---: | :---: | :---: | :---: | :---: | :---: 
1 | 15 | 32768^3 | 0.25 | 0.37 | 36
**2** | **14** | **16384^3** | **2** | **3** | **76**
3 | 13 | 8096^3 | 16 | 24 | 152
4 | 12 | 4096^3 | 128 | 190 | 228
5 | 11 | 2048^3 | 1025 | 1527 | 452

Notes: LX15 has only been run down to z = 6 for some of the halos. The rest are run down to z = 0. Timesteps are logarithm in expansion factor down to z = 6 (10 Myrs/snapshot) and linear in expansion factor down to z = 0 (50 Myrs/snapshot) for all runs. We have complete (modified) <span style="font-family:Courier">rockstar</span> halo catalogues (together with <span style="font-family:Courier">consistent-trees</span> merger trees) and z = 0 <span style="font-family:Courier">subfind</span> catalogues.

## Initial Conditions

Although we adopt a modified version of <span style="font-family:Courier">MUSIC</span> (v1.51), we include here for completeness our parameter file for our parent simulation from which all *Caterpillar* halos were extracted.

```Text
[setup]  
boxlength               = 100  
zstart                  = 127  
levelmin                = 10  
levelmin_TF             = 10  
levelmax                = 10  
padding                 = 8  
overlap                 = 4  
ref_center              = 0.5, 0.5, 0.5  
ref_extent              = 0.2, 0.2, 0.2  
align_top               = yes  
baryons                 = no  
use_2LPT                = no  
use_LLA                 = no  
periodic_TF             = yes  

[cosmology]  
Omega_m                 = 0.3175          
Omega_L                 = 0.6825          
Omega_b                 = 0.0489991       
H0                      = 67.11           
sigma_8                 = 0.8344         
nspec                   = 0.9624          
transfer                = eisenstein  

[random]  
seed[10]                = 34567  

[output]  
format                  = gadget2  
filename                = ./ics  
gadget_num_files        = 128  

[poisson]  
fft_fine                = yes  
accuracy                = 1e-5  
pre_smooth              = 3  
post_smooth             = 3  
smoother                = gs  
laplace_order           = 6  
grad_order              = 6 

```

Our <span style="font-family:Courier">P-Gadget3/Gadget4</span> flags used in our configuration file are as follows:

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
