# TheFullMulti_River_v2.0
New version of The Full Multi River model after correction of several bugs found in the original model code [TheFullMulti_RIVER](https://github.com/Nano2PlastProject/TheFullMulti_RIVER)


### Requirements
- Python 3.9.7
- Required packages: see `requirements.txt`

The corrections include:

- Bugs in the calculation of mixing rates between the surface, flowing and stagnant water compartments have been corrected to properly reflect the configuration described in Domercq et al. 2022 (Table S2). Mixing rates between stagnant water and sediment layer have been removed.

- Biofouling of already biofouled particles (i.e. "Biofouled-MP" and "heteroagg-Biofouled-MP") has been removed.

- Changes in the estimation of the fragmentation rates of biofouled particles have been introduced to only take the internal diameter of the biofouled particle (i.e. excluding the biofilm layer).

- Changes in the estimation of the rates of heteroaggregation of biofouled particles and of heteroaggregate breackup of biofouled and heteroaggregated particles have been introduced to use use the size of the aggregate (i.e. radius of parent particle + biofilm thickness and radius of parent particle + biofilm thickness + SPM radius respectively).

- Bug on the built up of the interactions dataframe have been corrected to properly assign interaction rates (some errors where found in the assignment of breack-up and biofouling rates as well as for sediment transport and advective transport).

All these corrections have resulted in sligth changes on the outputs of the model that are reflected in the rate constants heat maps and multigraphs of particle concentration distribution along the different compartments, particles species over the generic river profile. However, none of these changes affect the rational behing The Full Multi modelling framework, on the contrary they reinforce the importance of the highlighted concept of working with open source models where the user comunity can survey and improve over time such tools to make them stronger.

We would like to aknowledge the contributions made by Dr. Isamu Ogura (Research Institute of Science for Safety and Sustainability (RISS) National Institute of Advanced Industrial Science and Technology (AIST), Japan) by pointing out the bugs here described wich allowed us to perform the needed corrections of the Full Multi code.


### Authors
===========

Repository and Jupyter Notebooks: Dr. Maria del Prado Domercq (@PradoDomercq)

Coding of python files and functions: Dr. Antonia Praetorius (@apraetorius) and Dr. Maria del Prado Domercq (@PradoDomercq)

Contact:

fullMultiModel@aces.su.se
