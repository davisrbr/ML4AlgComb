# Symmetric group characters (classic result)

One way to understand the algebraic structure of permutations (symmetric groups, $S\_n$) is through their representation theory \[1\], which converts algebraic questions into linear algebra questions that are often easier to solve. 
A *representation* of group $G$ on vector space $V$, is a map $\phi:G \rightarrow GL(V)$ converts elements of $g$ to invertible matrices on vector space $V$ and which respects the compositional structure of the group. A basic result in representation theory says that all representations of a finite group can be decomposed into atomic building blocks called *irreducible representations*. Amazingly, irreducible representations are themselves uniquely determined by the value of the trace, $\text{Tr}(\phi(g))$, where $g$ ranges over subsets of $G$ called conjugacy classes. These value are called *characters*. 

The representation theory of symmetric groups has rich combinatorial interpretations. Both irreducible representations of $S\_n$ and the conjugacy classes of $S\_n$ are indexed by partitions of $n$ and thus the characters of irreducible representations of $S\_n$ are indexed by two partitions of $n$. For $\lambda,\mu \vdash n$ we write $\chi^\lambda\_\mu$. This combinatorial connection is not superficial, there are algorithms (e.g., the Murnaghan-Nakayama rule), which allow calculation of irreducible characters via simple manipulation of the Young diagrams for $\lambda$ and $\mu$ without any reference to algebra. 

**Dataset:** Pairs of integer partitions of $n$, $\lambda, \mu$ and the corresponding symmetric group character $\chi^{\lambda}\_{\mu}$.

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


