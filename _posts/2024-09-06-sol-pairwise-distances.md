---
layout: post
title: (SOLUTION) Pairwise Distance Patterns
categories:
  - solutions
permalink: solutions/sol_pairwise_distances/
hideinfeed: true
---
 *This solution showcases one method for restricting $n$. If you've come up with a different restriction, I'd love to hear it! You can contact me [here](/about/).*
 
Unless $n$ or $n-2$ is a square number, no solution is possible.

## Proof:
As with almost all parity proofs, we start by imagining our infinite grid to be a checkerboard. Note that if two pieces are on the same coloured square, the distance between them must be even, and if they are on different colours, the distance must be odd.

Suppose $b$ is the number of pieces that lie on black squares. Then, the number of odd distance pairs for a given $b$ is given by $b(n-b)$, which is the number of possible black-white pairs. The number of even distance pairs is then ${n \choose 2} - b(n-b)$.


We will examine two cases: ${n \choose 2}$ can be either even or odd.

#### If even:
*Since the number of pairs is even, and we need pairs of each distance from 1 to ${n \choose 2}$, we have an equal amount of even distance pairs and odd distance pairs. This gives us the following equation:
$$b(n-b) = {n \choose 2} - b(n-b)$$
This is a quadratic in $b$, so we can easily solve, and we obtain that $b = \frac{n \pm \sqrt{n}}{2}$. This is an integer if and only if $n$ is square. The number of black pieces clearly has to be an integer, so if ${n \choose 2}$ is even, then $n$ must be square for a solution to be possible.*

#### If odd:
*This is much the same as the last one. We note we'll have one more odd pair than even, and so:
$$b(n-b) = {n \choose 2} - b(n-b) + 1$$
This solves to $b = \frac{n \pm \sqrt{n-2}}{2}$. Hence, if ${n \choose 2}$ is odd, then $n-2$ must be a square number for a solution to exist.*

In both these cases, we obtain two roots, $r_{1}$ and $r_{2}$, but in both cases, $r_{2} = n - r_{1}$, showing that there's nothing special about counting the number of black pieces, we could just as easily switch.

Therefore, unless $n$ or $n-2$ is square, no solution is possible.

*Sadly, this says nothing about whether a solution is possible when the above conditions are met. If you have any ideas, let me know!*
