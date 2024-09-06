---
layout: post
title: Pairwise Distance Patterns
categories:
  - problems
permalink: problems/pairwise_distances/
---
You have an infinite grid, and $n$ pieces. We can measure the distance between two placed pieces using [Taxicab Distance](https://en.wikipedia.org/wiki/Taxicab_geometry).

With $n$ pieces, there are ${n \choose 2}$ possible pairs. Your goal is to place the pieces in such a way that there is exactly one pair of distance 1, exactly one pair of distance 2, exactly one pair of distance 3 and so on until exactly one pair of distance ${n \choose 2}$.

**An example for $n=3$**:

Place the pieces $A = (0,0)$,  $B = (0,1)$, and $C=(0,3)$. Then, $A \rarr B = 1$, $B \rarr C = 2$ and $B \rarr C = 3 = {3 \choose 2}$

Is this possible for all $n$? Why or why not?

### Hint
*highlight spoilers to read them*

{: .spoiler}
It is not possible for all $n$. There is exactly one $n  \leq 6$ with no solutions. Can you find which one, and prove that it has no solutions?

*A solution can be found [here](/solutions/sol_pairwise_distances/)*
