# QAP-instances
Various sets of QAP instances

## Available sets

Provided in different sub-directories:

* QAPLIB: the well-known suite (139 instances)
* QAPLIB-More: other (intermediate) instances of QAPLIB problems
* Drezner: Drezner instances
* Palubeckis: Palubeckis instances
* Taillard-Grey: Taillard grey patterns
* Carvalho-Rahmann: Carvalho & Rahmann microarray layout instances (to come)

## File formats

This project provides 3 file formats:

**Data file format: suffix: `.dat` (as provided by QAPLIB)**:

        SIZE
        flow/weight matrix (SIZE x SIZE values)
        distance matrix (SIZE x SIZE values)


We have extended this format (suffixed .qap) to record the optimum (when known) or a lower bound (e.g. computed with relaxations algorithms) and the best known solution (BKS).

This is done by extending the first line of the file (so most code remain compatible since the first line is treated separately).

**Data file format enriched, suffix: `.qap`:**


        SIZE  OPT  BKS
            OPT: optimal cost if OPT >= 0, else optimum is unknown but a known lower bound is -OPT
            BKS: the best known solution
        flow/weight matrix (SIZE x SIZE values)
        distance matrix (SIZE x SIZE values)

**Solution file format, suffix: `.sln` (as provided by QAPLIB):**

        SIZE COST
        vector of SIZE values

Beware: the vector of values can be 1-based (values in 1..SIZE) as provided by QAPLIB or 0-based (in 0..SIZE-1).

### See also
[The QAPLIB web site](http://www.mgi.polymtl.ca/anjos/qaplib/inst.html)


[The Taillard web site](http://mistic.heig-vd.ch/taillard/problemes.dir/qap.dir/qap.html) includes Taillard's hard instances and grey patterns and other author instances (e.g. Drezner).

**Carvalho and Rahmann**

In 2006, Carvalho and Rahmann proposed a new modeling for the placement problem in DNA microarrays layouts as a QAP. They propose a set of 14 problems which are intended to minimize either the border length problem or the conflict index problem in DNA microarrays. In their paper, these problems were solved using the GRASP metaheuristic. These problems turned out to be very difficult to solve, and therefore some researchers have included these problems to evaluate the performance of new algorithms.

Sergio A. de Carvalho and Sven Rahmann.  *Microarray Layout as Quadratic Assignment Problem*. German Conference on Bioinformatics GCB 2006, Tübingen, Germany.








