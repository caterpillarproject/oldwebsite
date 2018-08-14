---
layout: page
title: About
image:
  feature: header.jpg
  credit: Caterpillar Collaboration
  creditlink: http://www.caterpillarproject.org
comments: false
reading_time: false
modified: 2018-08-03
---

The Caterpillar project a state-of-the-art cosmological simulation suite consisting of dark matter halos of mass similar to that of our own Milky Way. 

The full Caterpillar catalogue consists of ~40 dark matter halos at a particle resolution of ∼10<sup>4</sup> M<sub>⊙</sub> making it one of the largest and highest resolution simulation suites of its kind in the world to date. These data are enabling us to statistically probe the formation history and evolution of all galaxies of similar size to the Milky Way, including the Milky Way itself!

All of following information is detailed in our flagship paper [Griffen et al. (2015)](http://adsabs.harvard.edu/cgi-bin/bib_query?arXiv:1509.01255).

Head to our [documentation](http://docs.caterpillarproject.org) to get more detail on our simulation technique and process as well as how to obtaining access.

## A Brief History

The Caterpillar project was the brainchild of Profs. Anna Frebel and
Lars Hernquist at the CfA in ~2010. In 2012, Phillip Zukin was then a
PhD student under Edmund Bertschinger at MIT who was temporarily
employed to carry out the first parent volume simulations that would
become the Caterpillar project. His work continued until Brendan Griffen
arrived as the new postdoc to take charge of the project in its entirety
in late 2012. Graduate students Greg Dooley and Alex Ji also contributed heavily to the project throughout their PhD at MIT. At a conference at UC Irvine in early 2014 between Anna Frebel, Brian O'Shea, Brendan Griffen and Facundo Gomez, it
was agreed that we would combined datasets and future efforts (Brian and
Facundo had a similar sized project for studying stellar halos at the
time). In September of 2015, the first Caterpillar paper was put [on the
arxiv](http://adsabs.harvard.edu/cgi-bin/bib_query?arXiv:1509.01255).

## Motivation

The Caterpillar project is a large simulation suite of dark matter halos
of mass similar in size to that of the Milky Way. By virtue of the
extremely large number of halos, temporal and spatial resolution of the
simulations, it is one of the largest simulation suites of its kind in the
world. We plan to extend the initial release sample to 40 halos in
total.

The goal of the Caterpillar Project is to use these relatively
inexpensive dark matter simulations to:

-  statistically probe the merger history of Milky Way-like galaxies,
-  understand the origin and evolution of the satellite systems of Milky
   Way-like galaxies and
-  determine to what extent the Milky Way is unusual relative to its
   similar sized cousins.
-  probe the earliest progenitors of the Milky Way and determine the
   properties of their surviving populations.

Please [click here](/motivation/) for a much more detailed outline of our motivation.

Approach
------------------

The *Caterpillar* suite was run using <span style="font-family:Courier">P-Gadget3</span> and <span style="font-family:Courier">Gadget-4</span>, tree-based
*n*-body codes based on <span style="font-family:Courier">Gadget-2</span> (Springel et al. 2005). All initial
conditions were constructed using music (Hahn & Abel 2011). We identify
dark matter halos via Rockstar (Behroozi et al. 2013) and construct
merger trees using <span style="font-family:Courier">consistent-trees</span> (Behroozi et al. 2012). <span style="font-family:Courier">ROCKSTAR</span>
assigns virial masses to halos, \\(M_{vir}\\), using the evolution of
the virial relation from Bryan & Norman (1998). for our particular
cosmology. At *z* = 0, this definition corresponds to an over-density of
104x the critical density of the Universe. We have modified <span style="font-family:Courier">ROCKSTAR</span> to
output *all* particles belonging to each halo so we can reconstruct any
halo property in post-processing if required. We have also improved the
code to include iterative unbinding. In our work, we restrict our
definition of virial mass to include only those particles which are
bound to the halo.


## Cosmological Parameters

We adopt a [Planck 2013 Cosmology](http://adsabs.harvard.edu/cgi-bin/bib_query?arXiv:1303.5076).

  \\(\Omega_{\Lambda}\\) | \\(\Omega_{m}\\) | \\(\sigma_{8}\\) | \\(n_{s}\\) | \\(h\\)
  :---: | :---: | :---: | :---: | :--:
  0.68  | 0.31  | 0.83  | 0.96  | 0.67

## Parent Simulation

  Volume <br> *h*<sup>-3</sup> Mpc<sup>3</sup> | # particles  | \\(m_{dm}\\) <br> 10<sup>7</sup> \\(M_\odot\\) | \\(\epsilon_{dm}\\) <br> pc 
  :---: | :---: | :---: | :---: 
        100<sup>3</sup>          | 1024<sup>3</sup> | 12 | 2441 

<img src="{{ site.url }}/images/parent.jpg">
<center>
The parent simulation. Width is 100 Mpc h<sup>-1</sup>.
</center>

## Caterpillar (zoom-in) Simulations

The Caterpillar suite is a zoom-in suite where regions of interest from the parent simulation are sampled and re-run at much higher resolution. The following table describes the range of levels run and compares them to the seminal Aquarius suite.

~*Aquarius* <br> Level | MUSIC <br> *levelmax* | Effective <br> Resolution | \\(m_{dm}\\) <br> 10<sup>4</sup> *h*<sup>-1</sup> \\(M_\odot\\) | \\(m_{dm}\\) <br> 10<sup>4</sup> \\(M_\odot\\) | \\(\epsilon_{dm}\\) <br> pc 
  :---: | :---: | :---: | :---: | :---: | :---: 
1 | 15 | 32768<sup>3</sup> | 0.25 | 0.37 | 36
**2** | **14** | **16384<sup>3</sup>** | **2** | **3** | **76**
3 | 13 | 8096^3 | 16 | 24 | 152
4 | 12 | 4096^3 | 128 | 190 | 228
5 | 11 | 2048^3 | 1025 | 1527 | 452

Notes: LX15 has only been run down to z = 6 for some of the halos. The rest are run down to z = 0. Timesteps are logarithm in expansion factor down to z = 6 (10 Myrs/snapshot) and linear in expansion factor down to z = 0 (50 Myrs/snapshot) for all runs. We have complete (modified) <span style="font-family:Courier">rockstar</span> halo catalogues (together with <span style="font-family:Courier">consistent-trees</span> merger trees) and z = 0 <span style="font-family:Courier">SUBFIND</span> catalogues.

Here are the first 24 Caterpillar zoom-in halos:

<div class="row-images-halos">
  <div class="column-images-halos">
    <img src="{{ site.url }}/images/halos/Cat1.jpg">
    <img src="{{ site.url }}/images/halos/Cat5.jpg">
    <img src="{{ site.url }}/images/halos/Cat9.jpg">
    <img src="{{ site.url }}/images/halos/Cat13.jpg">
    <img src="{{ site.url }}/images/halos/Cat17.jpg">
    <img src="{{ site.url }}/images/halos/Cat21.jpg">
  </div>
  <div class="column-images-halos">
    <img src="{{ site.url }}/images/halos/Cat2.jpg">
    <img src="{{ site.url }}/images/halos/Cat6.jpg">
    <img src="{{ site.url }}/images/halos/Cat10.jpg">
    <img src="{{ site.url }}/images/halos/Cat14.jpg">
    <img src="{{ site.url }}/images/halos/Cat18.jpg">
    <img src="{{ site.url }}/images/halos/Cat22.jpg">
  </div>
  <div class="column-images-halos">
    <img src="{{ site.url }}/images/halos/Cat3.jpg">
    <img src="{{ site.url }}/images/halos/Cat7.jpg">
    <img src="{{ site.url }}/images/halos/Cat11.jpg">
    <img src="{{ site.url }}/images/halos/Cat15.jpg">
    <img src="{{ site.url }}/images/halos/Cat19.jpg">
    <img src="{{ site.url }}/images/halos/Cat23.jpg">
  </div>
  <div class="column-images-halos">
    <img src="{{ site.url }}/images/halos/Cat4.jpg">
    <img src="{{ site.url }}/images/halos/Cat8.jpg">
    <img src="{{ site.url }}/images/halos/Cat12.jpg">
    <img src="{{ site.url }}/images/halos/Cat16.jpg">
    <img src="{{ site.url }}/images/halos/Cat20.jpg">
    <img src="{{ site.url }}/images/halos/Cat24.jpg">
  </div>
 </div>

If you would like more details, please see our flagship paper, [Griffen et al. (2015)](http://adsabs.harvard.edu/cgi-bin/bib_query?arXiv:1509.01255).
