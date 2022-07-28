# README SetOfProductsReduce
----------------------------

Author: Myriam DUPRAZ, intern for 3 months (May-July 2022) at RISC (Linz, Austria), supervised by Carsten SCHNEIDER
Date: July 2022
Language: Mathematica

----------------------------

# Purpose
The code aims at helping the user representing products efficiently. Products are symbolized by P-monomials, i.e. triples {p[i],alpha,0}, the set of which being called a "P-extension",
such that alpha belongs to some rational field  Z(x,y_i...).
and TSigma[p[i]]/p[i]= alpha.

# Organisation of the project
The project contains three directories:
* code/ contains files.nb of Mathematica code,ready to use
* text-of-the-code/ contains files.txt with the exact Mathematica code, ready to copy/paste, impossible to run rightaway, but possible to read without need of Mathematica software 
* tests/ contains files.txt with texts inputs ready to copy/paste in a Mathematica sheet, and files.pdf with some examples of inputs and outputs

# Organisation of the code and dependancies
The code is split into 4 parts, to which a fifth part generating test cases is added.
1. Evaluation
2. SetReduce
3. SynchroDegReduce
4. CombSetDegReduce
5. genRandomTest

All parts are dependant on package Sigma by C. Schneider. To access it, you should ask RISC here https://www3.risc.jku.at/research/combinat/software/Sigma/.
Please note the following further dependancies (-> stands for "required for"): 
1 -> 2,3,4
2,3 -> 4

# Contents
1. Evaluation : contains encoding of evaluation function, which can evaluate any element in some difference ring Z(x,y_i...)[z][p_j,p_j^-1...] described by a tower of 
shape {{x,1,1},{y_i,lamda_i,0}}...,{z,rho,0},{p_j,alpha_j,0}} given with fitrst indices necessary for the evaluation of the P-mononmials.
2. SetReduce: implementation of set's size reduction, i.e. computation of a Pi-extension of minimal size, and representations in it of the P-monomials of the input P-extension
3. SynchroDegReduce: implementation of 2 methods for degree reduction, simple and synchronized, i.e. computation of a P-extension with P-monomial with alphas of minimal degree, and representations in 
it of the P-monomials of the input P-extension
4. CombSetDegReduce: implementation of 3 scenarios to get a degree-reduced AND set-reduced Pi-extension, and representations in it of the P-monomials of the input P-extension
5. genRandomTest: function to generate valid inputs, i.e. P-extensions and valid first indices for their evaluations, with alphas in the rational; field  rational field  Z(x).

# Howto
see the information associated to every function with ?NameOfFunction

# References
The algorithm used for Evaluation is built from [1].
The algorithm implemented in SetReduce comes from [2].
The algorithms implemented in SynchroDegReduce rely on [3], with notions previously introduced by [4] and [5].

[1] Term algebras, canonical representations and difference ring theory for symbolic summation,author={Schneider, Carsten},booktitle={Anti-Differentiation and the Calculation of Feynman Amplitudes},pages={423--485},year={2021},publisher={Springer}

[2] Minimal representations and algebraic relations for single nested products,author={Schneider, Carsten},journal={Programming and Computer Software},volume={46},number={2},pages={133--161},year={2020},publisher={Springer}

[3] Product representations in $\Pi\Sigma$-fields, author={Schneider, Carsten},journal={Annals of Combinatorics},volume={9}, number={1},pages={75--99},  year={2005}, publisher={Springer}

[4] Summation in finite terms,author={Karr, Michael},journal={Journal of the ACM (JACM)},volume={28},number={2},pages={305--350},year={1981},publisher={ACM New York, NY, USA}

[5] Rational normal forms and minimal decompositions of hypergeometric terms,author={Abramov, Sergei A and Petkov{\v{s}}ek, Marko},journal={Journal of Symbolic Computation},volume={33},number={5},pages={521--543},year={2002},publisher={Elsevier}
