# Calculating the characters of irreducible representations of the symmetric group (classic result)

One way to understand the algebraic structure of permutations (symmetric groups, $S\_n$) is through their representation theory \[1\], which converts algebraic questions into linear algebra questions that are often easier to solve. 
A *representation* of group $G$ on vector space $V$, is a map $\phi:G \rightarrow GL(V)$ converts elements of $g$ to invertible matrices on vector space $V$ and which respects the compositional structure of the group. A basic result in representation theory says that all representations of a finite group can be decomposed into atomic building blocks called *irreducible representations*. Amazingly, irreducible representations are themselves uniquely determined by the value of the trace, $\text{Tr}(\phi(g))$, where $g$ ranges over subsets of $G$ called conjugacy classes. These value are called *characters*. 

The representation theory of symmetric groups has rich combinatorial interpretations. Both irreducible representations of $S\_n$ and the conjugacy classes of $S\_n$ are indexed by partitions of $n$ and thus the characters of irreducible representations of $S\_n$ are indexed by pairs of partitions of $n$. For $\lambda,\mu \vdash n$ we write $\chi^\lambda\_\mu$. This combinatorial connection is not superficial, algorithms for computation of irreducible characters (e.g., the Murnaghan-Nakayama rule) which can be reduced to simple manipulation of the Young diagrams for $\lambda$ and $\mu$. That is, all the algebra is eliminated 

## Dataset 
Since the conjugacy classes of the symmetric group $S_n$ are indexed by integer partitions of $n$, characters are constant on conjugacy classes, and the irreducible representations of $S_n$ are also indexed by integer partitions of $n$, the task is to use a pair of integer partitions of $n$ to predict the character of the corresponding irreducible representation of the symmetric group.

Within each file, two integer partitions are provided followed by an integer corresponding to the character. For instance:

`[3,1,1],[2,2,1],-2`  

says that the character $\chi^{3,1,1}_{2,2,1} = −2$. We provide files for $n = 4, 5, 6$. These are named: 221
C.8.3
• sym_grp_char_18_train.txt • sym_grp_char_18_test.txt • sym_grp_char_20_train.txt • sym_grp_char_20_test.txt • sym_grp_char_22_train.txt • sym_grp_char_22_test.txt
**Task:** Given partitions $\lambda$ and $\mu$, predict the irreducible symmetric group character $\chi^{\lambda}\_{\mu}$.

Datasets can be found [here](https://drive.google.com/file/d/15AHAn9NnC7crzG_8BnaH3pp1aOGUUniV/view?usp=sharing).

### Logistic Regression

| Size | Accuracy | 
|----------|----------|
| $n= 18$ | $40.6 \pm 0.00%$ |
| $n= 20$  | $40.64 \pm 0.00%$ |
| $n= 22$  | $41.01 \pm 0.00%$ | 

### Transformer

| Size | Accuracy | 
|----------|----------|
| $n= 18$ | $42.19 \pm 0.00%$ |
| $n= 20$  | $41.92 \pm 0.00%$ |
| $n= 22$  | $41.61 \pm 0.00$ | 

\[1\] Sagan, Bruce E. The symmetric group: representations, combinatorial algorithms, and symmetric functions. Vol. 203. Springer Science & Business Media, 2013.


