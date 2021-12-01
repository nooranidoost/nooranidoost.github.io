---
layout: page
title: Bayesian Estimation of Biofilm Mechanics
permalink: /miscellany/item-0/
---

<!-- MathJax -->
<script defer type="text/javascript" id="MathJax-script" src="https://cdn.jsdelivr.net/npm/mathjax@3.1.2/es5/tex-mml-chtml.js"></script>
<script defer src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>

Bacterial pathogens inside biofilms grow by consuming the nutritious substrates available in the surrounding environment, and on the other hand contribute
to developing the polymeric network by producing extracellular eDNA and polysaccharides such as Psl, Pel, and Alginate. Despite the numerous research studies
on biofilm modeling, how the matrix properties affect biofilm structure, maturation, and the interactions between components of the biofilm are largely unexplored.

During my postdoctoral appointment, I worked on mathematical modeling and uncertainty quantification of biofilm models and bacterial community, in order to better
understand their structure and morphology. These models consist of a combination of springs and dashpots, representing the elasticity and viscosity of the 
substances, respectively. Using a Markov Chain Monte Carlo technique, which is based on a Bayesian inference, I successfully estimated the viscoelastic 
characteristics biofilm matrix, which helps us understand the composition of the biofilm at different stages of their development. MCMC method generates sample
candidates from a parameter space, that are either rejected or accepted based on our prior knowledge on the parameter space and the likelihood of the model.
The accepted candidates form the posterior distribution. The MCMC methods are based on the Bayes' theorem:

<p><span class="math display">\[\label{bayes}
\pi(\theta \vert y) = \frac{p(y\vert \theta) \pi_0(\theta)}{\int_{R}^{} p(y\vert \theta) \pi_0(\theta)\, d \theta}\]</span></p>

\noindent where $\pi(\theta \vert y)$ is our posterior distribution, the probability of the model given the observed data. $p(y\vert \theta)$ is the likelihood,
the probability of the observed data given the model. $P_0(\theta)$ is the prior distribution, the probability of the data, which can be interpreted as the prior
knowledge we have from the data. The integral term in the denominator is the integral of the numerator over the parameter space, which is a normalization factor 
and is fixed. I employed the Delayed Rejection Adaptive Metropolis (DRAM) algorithm developed by \cite{haario2006dram} to improve the efficiency and speed 
of the computations by increasing convergence and acceptance rate. 

I used a Burger viscoelastic model that contains a spring and a dashpot in series (Maxwell compartment), connected to a spring and a dashpot in parallel
(Kelvin-Voigt compartment). $E$ and $\eta$ represent spring and dashpot coefficients, respectively. The viscoelastic constitute equation for the Burger model 
is derived as:

<p><span class="math display">\[\label{burger}
\ddot \sigma (\frac{\eta_m \eta_k}{E_m E_k}) + \dot \sigma (\frac{\eta_m} {E_k} + \frac{\eta_m} {E_m} + \frac{\eta_k} {E_k}) + \sigma = \ddot \epsilon (\frac{\eta_m \eta_k}{E_m}) + \dot \epsilon\]</span></p>

\noindent where $\sigma$, $\epsilon$, $E$, and $\eta$ denote stress, strain, linear spring constant and linear dashpot constant, respectively. The underscripts
$m$ and $k$ represent Maxwell and Kelvin compartments in our Burger model. Using the DRAM algorithm, I estimated the four viscoelastic parameters 
($E_m, \eta_m, E_k,$ and $\eta_k$) during a creep-recovery test for three different biofilm colonies after 4 days of formation: 1) WT, that is a wild type of
\textit{P. aeruginosa} POA1 (Fig.~\ref{bf-fig:1}), 2) Rugose small-colony variants of POA1 (RSCV), that is a isogenic PAO1$\Delta$wspF, and 3) mucoid, that is 
the mucoid variant of POA1, PAO1mucA22. 

My further simulations of the three biofilms at two other stages of development: after 2 days and 6 days of formation, showed that the four viscoelastic
parameters do not follow a similar trend for the three biofilms, with WT being very sensitive, and subject to significant change over time. The changes
in viscoelastic properties of these three biofilms over time can be intrepreted as the change in the share of polymeric components such as Psl, Pel, and Alginate.
