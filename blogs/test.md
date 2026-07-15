
# Velocity Correlation for an Exponential Decay with Gaussian White Noise.
This is a short write up based on discussions with Soling, took place on [[2025-07-04]]. We were talking about the extend of correlation of an exponentially decaying random variable with a white noise. The dynamics of the system is described as
$$
\frac{dv}{dt} = -\alpha v +\xi(t)
$$
where $v$ is the state variable(also the random variable) and $\xi(t)$ is sampled from $\mathcal{N}(0, 1)$. 

To solve this, we define an integration factor $IF = e^{-\int P(t)dt}$, where $P(t) = -\alpha$ 
Thus,
$$
\begin{align}
IF &= e^{-(-\int \alpha dt)}\\
	&= e^{\alpha t}\\
\frac{d}{dt}[e^{\alpha t}] &= \alpha e^{\alpha t} 
\end{align}
$$
Multiplying the original equation with $IF$ and solve
$$
\begin{align}
e^{\alpha t} \cdot \frac{dv}{dt} &= -\alpha e^{\alpha t} \cdot v  +\xi(t) \cdot e^{\alpha t}\\
e^{\alpha t} \cdot \frac{dv}{dt} &=- \frac{d}{dt}[e^{\alpha t}]v  +\xi(t) \cdot e^{\alpha t}\\
\int e^{\alpha t} \cdot dv &= -\int \frac{d}{dt}[e^{\alpha t}]\cdot v \cdot dt  +\int \xi(t) \cdot e^{\alpha t} \cdot dt\\
\int d[e^{\alpha t} \cdot v]&= - ve^{\alpha t} + \int e^{\alpha t} \xi(t)\cdot dt +c \\
 \cdots \\ 
 v(t) &= \int e^{\alpha t} \xi(t)\cdot dt +c
\end{align}
$$The velocity correlation is, 
$$
\begin{align}
\langle v(t)\cdot v(t')\rangle &=  \bigg\langle \bigg(\int e^{\alpha t} \xi(t)\cdot dt +c\bigg)\bigg( \int e^{\alpha t'} \xi(t')\cdot dt' +c\bigg) \bigg\rangle\\
&=c^2+ \bigg\langle c\bigg(\int e^{\alpha t} \xi(t)\cdot dt + \int e^{\alpha t'} \xi(t')\cdot dt'\bigg)\bigg\rangle \\& + \bigg\langle \iint e^{\alpha (t+t')}\cdot  \xi(t)\xi(t')\cdot dt \cdot dt' \bigg\rangle \\
\langle vv'\rangle &= c^2 + \bigg\langle \iint e^{\alpha (t+t')}\cdot  \xi(t)\xi(t')\cdot dt \cdot dt' \bigg\rangle \\
\end{align}
$$

