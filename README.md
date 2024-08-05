# GADFly
_**Genetic Algorithm for Discriminant Function Analysis**_

**Introduction**.

This application is a fully contained cloud service running on the MS Azure platform.  The genetic algorithm is written in transact-SQL.  Scripts for this part of the application are supplied here in **GADFly Algorithm.txt**.

_A Note on terminology_.  As this is a genetic algorithm, more correctly, an evolutionary algorithm, I have used the biological terms "population", "genome", "gene" and "codon" to represent the hierarchy of objects used by the algorithm.  They do not reference the data being analysed in any way.  

Briefly, the algorithm takes a "population" of randomly generated predictive rules ("genomes") and evolves them to best predict a binary target variable.  The "genomes" comprise a number of logical expressions ("genes") that each evaluate to TRUE or FALSE.  These are combined into "genomes" with AND or OR conjunctions which, as a whole, evaluate to TRUE or FALSE.  In turn, the "genes" comprise one or more "codons" which are the individual predictor variables, combined with arithmetic operators such as + or *.  Over a larger number of "generations", the algorithm modifies the individual "genomes" using processes such as "mutation", "insertion" or "recombination".  "Genomes" with strong predictive power are retained in the "population", with the lowest scoring "genomes" dying out from each generation.  In this way, the "population" evolves to contain a set of the best predictive rules ("genomes"). 

Predictive power is assessed by using the phi-coefficient, which measures the degree of association between two binary variables.  It has three penalties, which account for a) the number of null values in the predictor variables, b) the number of "genes" and c) the number of "codons" in the "genome".

The GUI is implemented in ASP.NET which is currently under final development.


**SMC Poulton**

5th August 2024
