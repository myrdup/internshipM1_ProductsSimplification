README SetOfProductsReduce
----------------------------
Author: Myriam DUPRAZ, intern for 3 months (May-July 2022) at RISC (Linz, Austria)
----------------------------
Date: July 2022
----------------------------

# Purpose
The code aims at helping the user representing products efficiently. Products are symbolized by P-monomials, i.e. triples {p[i],alpha,0}, the set of which being called a "P-extension",
such that alpha belongs to some rational field  Z(x,y_i...).
and TSigma[p[i]]/p[i]= alpha.

# Organisation and dependencies
The code is split into 4 parts, to which a fifth part generating test cases is added.
1. Evaluation
2. SetReduce
3. SynchroDegReduce
4. CombSetDegReduce
5. genRandomTest

All parts are dependant on package Sigma by C. Schneider. 
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

# Test design
Test files .txt are available to get inputs for every function
Test files .pdf contain some examples with their outputs
