# Replicator Dynamics

Notes from [Hofbauer-Sigmund](https://www.cambridge.org/core/books/evolutionary-games-and-population-dynamics/A8D94EBE6A16837E7CB3CED24E1948F8)
___
# Evolutionarily  stable strategies
## Hawk- Dove/Chicken/Snowdrift game
- $G$ is the value of contested resource
- $C$ is the cost of fight escalation. 
- $C>G>0$.
$$
\begin{pmatrix} \frac{G-C}{2} & G\\ 0 & \frac{G}{2}
\end{pmatrix}
$$
Let $x$ be the population of hawks and $1-x$ be the population of doves. Then the average increase in fitness for hawks,   

$$
\langle f(H)\rangle = \frac{G-C}{2}x + G(1-x)
$$ Average increase in fitness for doves, 
$$
\langle f(D)\rangle = \frac{G}{2}(1-x)
$$For both the species to coexist, 
$$\begin{align}
\langle f(H)\rangle =& \langle f(D)\rangle \\
\frac{G-C}{2}x+G(1-x) =&\frac{G}{2}(1-x)\\
\implies x =& \frac{G}{C}
\end{align}$$
If $x<\dfrac{G}{C}$ , Hawks get to spread and if $x$ is larger they shrink to $\dfrac{G}{C}$.  If you let the system evolve it will set to this stable state eventually.

## Evolutionary stability
Let $W(I, Q)$ be the fitness of an individual of type $I$ in a population of composition $Q$. $xJ+(1-x)I$ be the population with type $J$ of frequency $x$ and type $I$ of frequency $(1-x)$.  A population of type $I$ is said to be *evolutionarily stable* if
$$
W(J, \epsilon J+(1-\epsilon)I)< W(I, \epsilon J+(1-\epsilon)I)
$$
for all sufficiently small $\epsilon>0$. 
- Later book goes on with two examples: hawk-dove game and sex-ration game
## Normal form games
Let there be $N$ pure strategies such as $R_1, R_2\cdots, R_N$ and mixed strategies where each pure strategy is played with some probability. They form the strategy space $S_N$  and a strategy is a point $\textbf{p}$ in it. 
$$
S_N =\left\{ \textbf{p} = (p_1, p_2, \cdots ,p_N)\in \mathbb{R}^N: p_i\geq 0 \text{~and~}\sum_{i=1}^N p_i=1\right\}
$$
Let $u_{ij}$ be the payoff for a player playing strategy $R_i$ against $R_j$. The payoff for a $\textbf{p}$-strategist against $\textbf{q}$-strategist is
$$
\textbf{p}\cdot U\textbf{q} = \sum_{ij}u_{ij}p_iq_j
$$
$$
	\beta(\textbf{q}) = \max  \{ \textbf{p}\rightarrow \textbf{p}\cdot U\textbf{q}\}
$$
$\beta$ is a non empty boundary face of $S_N$. 
Nash equilibrium is a strategy which is a best reply to itself. Every normal form game admits at least one Nash equilibrium . For a **strict Nash equilibrium**, $\textbf{q}$
$$
\textbf{p}\cdot U\textbf{q} < \textbf{q} \cdot U\textbf{q}; \quad \forall \textbf{q}\neq \textbf{p} 
$$
## Evolutionarily stable strategies


# Replicator dynamics
- Nash equilibria  and ESS in terms of replicator dynamics. 
-  Replicator dynamics' equivalence to Lotka- Volterra equation. 
- Analysis of rock-paper-scissors game and partnership game

## Replicator equation
Assume a population is divided into $n$ types $E_1, \cdots E_n$ with frequencies $x_1,\cdots,x_n$. The fitness $f_i$ of $E_i$ is a function of the population composition $\text{x}$. The rate of increase of each type is based on their evolutionary success and we set it to be the difference between individual fitness $f_i$ and average fitness of population. If we assume a large enough population and if the generations blend continuously into each other we may assume that $\textbf{x}(t)$ evolves in $S_n$ continuously and the evolution is captured by the replicator equation
$$
\dot{x_i} = x_i\left( f_i(\text{x})-\sum f_i x_i \right) \quad i=1, 2, \cdots, N
$$
