---
layout: page
title: Research
permalink: /miscellany/
---

<!-- MathJax -->
<script defer type="text/javascript" id="MathJax-script" src="https://cdn.jsdelivr.net/npm/mathjax@3.1.2/es5/tex-mml-chtml.js"></script>
<script defer src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>

My research work revolve around the development of theoretical and numerical models for studying the bio-mechanical systems, and complex flows. Physics of fluids in these systems are important to a variety of applications, including: 1) bacterial community and biofilm formation, where biofilm can be modeled as a multi-scale system, 2) cell-biomechanics, where the focus is on the behavior of single cells, cell mechanical properties and interactions between cells in extracellular environment, and 3) complex flows which exhibit rheological behavior.

In the case of such complex systems, where the physics is not fully explored, mathematical models can be coupled with experiments to better predict and optimize the relevant parameters involved in the problem. Parameter estimates are fundamental for a range of predictive analysis including optimal control, sensitivity and uncertainty. However, these data assimilation techniques are much less widespread in biomathematics applications where the challenges are unique. I develop numerical platforms based on Bayesian statistics to assimilate observational data to estimate parameters in a variety of settings, primarily in mechanics where the topic is underdeveloped.

During my postdoctoral career at the Florida State University, I had the opportunity to work closely with Dr. Cogan and Dr. Huusani on mathematical modeling and uncertainty quantification of biofilm mechanics. The heterogeneity of the biofilm composition and its dynamic behavior require detiled investigations. The bacteria colony in the biofilm produce various types of extracellular polymeric substances such as Psl, Pel, and alginate, which are involved in biofilm development, attachment to the surface and structure integrity. The viscoelastic characteristics of such polysaccharides are not fully explored in literature due to their complexity, and is the subject of my research. At the same time, there is renewed interest in the biomechanics of biofilms due recent advances in understanding of the key signaling pathways controlling polymer production. I have estimated mechanical parameters of biofilms, along with our experimental collaborators, Dr. Stoodley and Dr. Gloag (Ohio state University). For the next step of this work, I will use dynamical systems and PDE viscoelastic models to build a robust mathematical model for development and spatiotemporal arrangement of biofilm components, including rheological and kinetics models. The mathematical model will be coupled with stochastic Bayesian algorithms to quantify the uncertainty and estimate  the relevant model parameters. This understanding will be useful for targeted treatments designed to manipulate the biofilm, making it easier to remove.


During my master’s study at the Koc University and Ph.D. at the University of Central Florida, I had the opportunity to work on various projects and collaborated with amazing research teams. My work was focused specifically on numerical simulations of complex rheological and biological flows in droplet based microfluidic systems. For these projects, I modeled the governing fluid flow equations by an incompressible Navier-Stokes equations which were solved in the framework of a one-field formulation on an Eulerian grid for all fluids. These continuity and momentum equations can be expressed as:

<p><span class="math display">\[\begin{aligned}
\nabla\cdot \textbf{u} &amp;=&amp; 0, \label{continuity_eq} \\
\frac{\partial \rho \textbf{u}}{\partial t} + \nabla\cdot(\rho \textbf{uu}) &amp;=&amp;-\nabla p + \nabla\cdot\mu_{s}(\nabla\textbf{u}+\nabla\textbf{u}^T) + \nabla\cdot \pmb{\tau}  + \int_A \sigma \kappa{\bf n}\delta({\bf x} - {\bf x_f})dA,
\label{NS_eq}\end{aligned}\]</span></p>

\noindent where $\rho$, $\mu_s$, $p$ and \textbf{u} denote the density, solvent viscosity, pressure, velocity vector, and $\pmb{\tau}$ is the viscoelastic extra stress tensor. The last term in the momentum equations represents the interfacial tension, where $\sigma$ is the interfacial tension coefficient, $\kappa$ is the mean curvature, $\bf n$ is the outward unit vector normal to the interface, and $\delta$ is the three-dimensional delta function. The interfacial tension force acts only on the interface location denoted by $\bf x_f$ which is solved on a Lagrangian grid and then is projected on the Eulerian grid to discrete momentum equation. The viscoelastic fluids were modeled using the FENE-CR model given by:

<p><span class="math display">\[\begin{aligned}
\frac{\partial \textbf{A}}{\partial t} + \nabla\cdot(\textbf{u}\textbf{A}) 
- (\nabla\textbf{u})^T\cdot\textbf{A} - \textbf{A}\cdot\nabla\textbf{u}
&amp;=&amp; - \frac{L^2}{L^2-{\rm trace}(\textbf{A})} \frac{\textbf{A} - \textbf{I}}{\lambda}, \label{stress_eq} \\
\pmb{\tau} = \mu_{p} \left(\frac{L^2}{L^2-{\rm trace}(\textbf{A})}\right) \frac{\textbf{A} - \textbf{I}}{\lambda},\label{stress_eq2}\end{aligned}\]</span></p>


where \textbf{A}, $\lambda$, $L$, \textbf{I}, and $\mu_p$ are the conformation tensor, the relaxation time, the extensibility parameter (i.e., the ratio of the length of a fully extended polymer dumbbell to its equilibrium length), the identity tensor, and polymeric viscosity, respectively. The multiphase flow was resolved by a viscoelastic front-tracking method\cite{tryggvason2001front} that was developed by Izbassarov and Muradoglu\cite{izbassarov2015front}. In this method the field quantities are solved on a staggered Eulerian grid and the interfaces between different phases are tracked by a Lagrangian grid consisting marker points connected with elements which move by the calculated velocity field on the Eulerian grid\cite{tryggvason2001front,izbassarov2015front}. The spatial and time derivatives were approximated using central differences and first order explicit method, respectively. The viscoelastic convective term in viscoelastic model were treated by a fifth-order upwind WENO-Z scheme along with a log-conformation method to overcome high Weissenberg number to preserve the positive-definiteness of the conformation tensor \cite{izbassarov2015front}. Using these numerical methods, I simulated formation of droplets, deposition of cell-loaded droplets in bio-printing systems, and migration and encapsulation of cells in microfluidic channels. 

