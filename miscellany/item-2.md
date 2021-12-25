---
layout: page
title: Deposition of cell-loaded droplets in bio-printing systems
permalink: /miscellany/item-2/
---

<!-- MathJax -->
<script defer type="text/javascript" id="MathJax-script" src="https://cdn.jsdelivr.net/npm/mathjax@3.1.2/es5/tex-mml-chtml.js"></script>
<script defer src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>


Despite significant progress, cell viability continues to be a central issue in droplet-based bioprinting applications. Common bioinks exhibit viscoelastic behavior owing to the presence of long-chain molecules in their mixture. I computationally studied effects of viscoelasticity of bioinks on cell viability during deposition of cell-loaded droplets on a substrate using a compound droplet model. The inner droplet, which represents the cell, and the encapsulating droplet are modeled as viscoelastic liquids with different material properties, while the ambient fluid is Newtonian. Using a front-tracking method to solve multi-phase flow equations and a FENE-CR model to model polymers inside the bio-ink solution and the cell, I simulated the deposition of cell-loaded droplets on a flat surface during a bio-printing process. A slip-contact line model was used to treat the dynamic contact line between the droplet interface and the flat surface. A survival model based on the cell mechanical deformation is used to relate cell deformation to cell viability.

Simulations with different viscoelastic bio-inks showed that during the deposition, the polymers inside the bio-ink extends rapidly and creates a thin viscoelastic boundary layer near the surface and the encapsulating droplet spread on the solid surface. Then a cell viability model was used to compute the cell viability as a function of maximum instantaneous cell deformation. I demonstrated that adding viscoelasticity to the encapsulating droplet fluid can significantly enhance the cell viability, suggesting that viscoelastic properties of bioinks can be tailored to achieve high cell viability in droplet-based bioprinting systems. High cell viability was found to be achieved for bio-inks with high polymeric viscosity ratios and Weissenberg numbers. Above a critical Weissenberg number, cell viability remained constant and further increasing of viscoelasticity did not improve cell viability. The effects of the cell viscoelasticity are also examined, and it is shown that the Newtonian cell models may significantly overpredict the cell viability.

 <figure>
 <img src="/images/fig3.jpg" alt="Snow" class="centerImage" width="99%">
  <figcaption> (a) Evolution of a cell-loaded droplet impingement on a flatsurface. The  left  and  right  halves show  the  Newtonian  (Wi_d= 0)  and the  viscoelastic  (Wi_d=   10, β_d=0.9) encapsulating  droplets, respectively. (b) The calculated cell viability (η) for bio-inks with different polymeric viscosity ratios (βd) and Weissenberg numbers (Wid)</figcaption>
</figure> 

Droplet-based bio-printing systems is a state-of-art technology in creating artificial organs and this work can guide researchers in biomedical clinics to design the proper bio-ink for these systems in order to improve the cell survival during printing process. This work was supported by the Scientific and Technical Research Council of Turkey (TUBITAK), Grant No. 112M181, and the COST Action Grant No. MP1106.

<li><b>M. Nooranidoost</b>, D. Izbassarov, and M. Muradoglu.  <a href="https://https://aip.scitation.org/doi/abs/10.1063/1.5108824">A computational study of droplet-based bioprinting: Effects of viscoelasticity</a> <i>Physics of Fluids</i> 31.8 (2019): 081901.</li>

