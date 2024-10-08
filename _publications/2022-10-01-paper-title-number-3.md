---
title: "Load-Balancing Intense Physics Calculations to Embed Regionalized High-Resolution Cloud Resolving Models in the E3SM and CESM Climate Models"
author: "Peng, L., Pritchard, M., Hannah, W. M., Blossey, P. N., Worley, P. H., & Bretherton, C. S."
journal: 'Journal of Advances in Modeling Earth Systems'
paperurl: 'https://agupubs.onlinelibrary.wiley.com/doi/epdf/10.1029/2021MS002841'
citation: 'Peng, L., Pritchard, M., Hannah, W. M., Blossey, P. N., Worley, P. H., & Bretherton, C. S. (2022). Load- balancing intense physics calculations to embed regionalized high-resolution cloud resolving models in the E3SM and CESM climate models. Journal of Advances in Modeling Earth Systems, 14, e2021MS002841. https://doi. org/10.1029/2021MS002841'
---
We design a new strategy to load-balance high-intensity sub-grid atmospheric physics calculations restricted to a small fraction of a global climate simulation's domain. We show why the current parallel load balancing infrastructure of Community Earth System Model (CESM) and Energy Exascale Earth Model (E3SM) cannot efficiently handle this scenario at large core counts. As an example, we study an unusual configuration of the E3SM Multiscale Modeling Framework (MMF) that embeds a binary mixture of two separate cloud-resolving model grid structures that is attractive for low cloud feedback studies. Less than a third of the planet uses high-resolution (MMF-HR; sub-km horizontal grid spacing) relative to standard low-resolution (MMF-LR) cloud superparameterization elsewhere. To enable MMF runs with Multi-Domain cloud resolving models (CRMs), our load balancing theory predicts the most efficient computational scale as a function of the high-intensity work's relative overhead and its fractional coverage. The scheme successfully maximizes model throughput and minimizes model cost relative to precursor infrastructure, effectively by devoting the vast majority of the processor pool to operate on the few high-intensity (and rate-limiting) high-resolution (HR) grid columns. Two examples prove the concept, showing that minor artifacts can be introduced near the HR/low-resolution CRM grid transition boundary on idealized aquaplanets, but are minimal in operationally relevant real-geography settings. As intended, within the high (low) resolution area, our Multi-Domain CRM simulations exhibit cloud fraction and shortwave reflection convergent to standard baseline tests that use globally homogenous MMF-LR and MMF-HR. We suggest this approach can open up a range of creative multi-resolution climate experiments without requiring unduly large allocations of computational resources.

Why the existing physics column load-balancing infrastructure in the CESM and E3SM can be inefficient when presented with highly regionalized, high-intensity physics computations?

<p align="center">
<img width="700" alt="image" src='/images/LoadBalance_F1.png'>
</p>
<br />

<br />

Our solution to this problem 
<p align="center">
<img width="700" alt="image" src='/images/LoadBalance_F2.png'>
</p>
<br />

<br />

Generalized solution
<p align="center">
<img width="700" alt="image" src='/images/LoadBalance_F3.png'>
</p>
<br />

<br />

Real-geography hindcast experiments results
<p align="center">
<img width="700" alt="image" src='/images/LoadBalance_F4.png'>
</p>
<br />

<br />

