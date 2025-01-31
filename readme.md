# Smart Manufactoring Monitoring

---

## Description

This repository is to reproduce the empirical results for two products eventually completed in success under three sets of probabilistic selection strategies, namely (ProD, UD, PreD), (ProD, CUD, PreD), (ProD, OCUD, PreD).

Each folder gives the probabilistic BDI agent model under each combination of selection strategies.


For fast process of reproducing the exact probability result, we have compiled the resulted DTMCs.

1. the user can first download PRISM from http://www.prismmodelchecker.org/download.php


2. to get the probability of (ProD, UD, PreD) with the event trace [Aevent, e_product2], for example, the user can do a command line ```prism -dtmc -importtrans ProD_UD_PreD_Aevent_e_product2.tra ProD_UD_PreD.csl```. And it should return you the value of ```0.0462```.




