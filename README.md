# QAP-instances
Various sets of QAP instances

We provide 3 file formats:

Data file format: suffix: `.dat` (as provided by QAPLIB):

        SIZE
        flow/weight matrix (SIZE x SIZE values)
        distance matrix (SIZE x SIZE values)


We have extended this format (suffixed .qap) to record the optimum (when known) or a lower bound (e.g. computed with relaxations algorithms) and the best known solution (BKS).

This is done by extending the first line of the file (so most code remain compatible since the first line is treated separately).

Data file format enriched, suffix: `.qap`:


        SIZE  OPT  BKS
            OPT: optimal cost if OPT >= 0, else optimum is unknown but a known lower bound is -OPT
            BKS: the best known solution
        flow/weight matrix (SIZE x SIZE values)
        distance matrix (SIZE x SIZE values)

Solution file format, suffix: .sln (as provided by QAPLIB):

        SIZE COST
        vector of SIZE values

Available sets (in different sub-directories):

* QAPLIB: the well-known suite (139 instances)

* QAPLIB-More: other (intermediate) instances of QAPLIB problems


