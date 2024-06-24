# HYPA-DBGNN

You need to open this folder as a devcontainer to receive all needed dependencies.

## Getting Started

Run `experiment.ipynb` to reproduce results from the paper for HYPA-DBGNN and strong baselines.
We tried to keep the file as concise and self-containing as possible to make it easier for the reader to spot and understand the main contributions.
For model selection other than the max. epochs different parameters need to be defined in code but also fixed parameters already lead to a confirmation of the results.
We include reference implementations for HYPA-DBGNN, GCN and DBGNN.
Besides we attach the used data sets together with the used random splits.
The resources for other baselines can be found in the link provided by the paper [De Bruijn goes Neural: Causality-Aware Graph Neural Networks for Time Series Data on Dynamic Graphs](https://openreview.net/pdf?id=Dbkqs1EhTr).
Additionally, they initially provided the parsed path data sets.

## Original Data Set Licenses

Highschool2011 
- Creative Commons Attribution-NonCommercial-ShareAlike license
- http://www.sociopatterns.org/datasets/high-school-dynamic-contact-networks

Highschool2012
- Creative Commons Attribution-NonCommercial-ShareAlike license, 
- http://www.sociopatterns.org/datasets/high-school-dynamic-contact-networks

Hospital
- Creative Commons Attribution-NonCommercial-ShareAlike license
- http://www.sociopatterns.org/datasets/hospital-ward-dynamic-contact-network/

StudentSMS
- MIT
- https://figshare.com/articles/dataset/The_Copenhagen_Networks_Study_interaction_data/7267433/1

Workplace2016
- Creative Commons Public Domain Dedication license
- http://www.sociopatterns.org/datasets/contacts-in-a-workplace/