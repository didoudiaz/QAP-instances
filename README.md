# QAP-instances
Various sets of QAP instances

We provide 3 file formats:

Format .dat:

SIZE
flow/weight matrix (SIZE x SIZE values)
distance matrix (SIZE x SIZE values)

We have extended this format (suffixed .qap) to record the optimum (when known) or a lower bound (e.g. computed with relaxations algorithms) and the best known solution (BKS).

This is done by extending the first line of the file (so most code remain compatible since the first line is treated separately).
Format .qap:

SIZE  OPT  BKS
    if OPT < 0 then OPT is unknown but a lower bound is known to be -OPT
    BKS: the best known solution

flow/weight matrix (SIZE x SIZE values)
distance matrix (SIZE x SIZE values)

file .sln (solutions as provided by QAPLIB):

SIZE COST
vector of SIZE values


Available sets (in different sub-directories):

* QAPLIB: the well-known suite (139 instances)

* QAPLIB-More: other (intermediate) instances of QAPLIB problems


