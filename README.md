# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

## Proof that $O(\log_2 n) = O(\log_5 n)$


1. **Big-O Definition**: $f(n) \in O(g(n)) \iff \exists c > 0, n_0 \geq 1: f(n) \leq c \cdot g(n) \ \forall n \geq n_0$.

2. **Change of Base Formula**: $\log_a n = \frac{\log_b n}{\log_b a}$.



## Proof:

To prove $O(\log_2 n) = O(\log_5 n)$, have to show that $\log_2 n \in O(\log_5 n)$ and $\log_5 n \in O(\log_2 n)$. First, considering $\log_2 n \in O(\log_5 n)$. Using the change of base formula, $\log_2 n = \frac{\log_5 n}{\log_5 2}$. Let $c = \frac{1}{\log_5 2} > 0$ (since $\log_5 2$ is a positive constant). Then $\log_2 n \leq c \cdot \log_5 n \ \forall n \geq 1$, which satisfies the definition of $\log_2 n \in O(\log_5 n)$. 

Next,  need to consider $\log_5 n \in O(\log_2 n)$. Again, using the change of base formula, $\log_5 n = \frac{\log_2 n}{\log_2 5}$. Let $c = \frac{1}{\log_2 5} > 0$ (since $\log_2 5$ is a positive constant). Then $\log_5 n \leq c \cdot \log_2 n \ \forall n \geq 1$, which satisfies the definition of $\log_5 n \in O(\log_2 n)$.



## Conclusion:

Since $\log_2 n \in O(\log_5 n)$ and $\log_5 n \in O(\log_2 n)$, we can conclude that $O(\log_2 n) = O(\log_5 n)$. The base of the logarithm does not affect the asymptotic complexity because logarithms with different bases differ only by a constant factor.

## Sources 

For this I started by intially looking at how other people approached this. I looked at dcollins22 repoistory and that is where I used the idea of the change of base and he refrenced knowing it from last years class. After that I looked up the formula and did my best to understand it on the whiteboard. 

https://cs.stackexchange.com/questions/76361/asymptotic-relationship-of-logarithms-in-different-bases 
https://www.cuemath.com/change-of-base-formula/ 
https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/
