# Smart Manufactoring Monitoring

---

## Description

This repository aims to provide the streamlined instruction with minimal efforts to ensure the reproducibility of the empirical results in Table 1 for two products eventually completed in success under three sets of probabilistic selection strategies, namely (ProD, UD, PreD), (ProD, CUD, PreD), (ProD, OCUD, PreD).

Each folder gives the probabilistic BDI agent model under each combination of selection strategies.


To reproduce the exact probability result with minimal steps, we have compiled the resulted DTMCs.

1. Build the PRISM model checker 

 we have provided the source code (for Linux x86) downloaded directly from the PRISM website.

    - extract the prism source code
    - navigate to the folder as current path
    - simply run ```./install.sh```

To allow the binary dependencies to be discovered, please set these in your PATH:

```export PATH=./bins:./bins/prism-4.8-linux64-x86/bin:$PATH```


2. Apply model checker to provided DTMCs

To get the probability of (ProD, UD, PreD) with the event trace [Aevent, e_product2], for example, the user can do a command line ```prism -dtmc -importtrans ProD_UD_PreD_Aevent_e_product2.tra ProD_UD_PreD.csl``` where ProD_UD_PreD_Aevent_e_product2.tra stands for the revised DTMC after event trace [Aevent, e_product2] and ProD_UD_PreD.csl constains the property specification, namely P = ?[F "box_1_success" & "box_2_success"] in PCTL language. And it should return you the value of ```0.0462```.



