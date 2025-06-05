---
layout: page
title: Building an LIF Neuron. 
permalink: /scirbbles/LIF_neuron.md
---


## Case-1
The ordinary differential equation given below is a simple system with constant rate of change.$$
\frac{dV}{dt} = \frac{V_0}{\tau}
$$This has no fixed points.
If we were to solve this we would obtain solution if would be;
$$
V(t) = \frac{V_0}{\tau}\cdot t
$$The $V$ vs $t$ graph will be a line with slope, $m=\frac{V_0}{\tau}$.

## Case-2
Now we subtract the variable to make the equation bound to a maxima
$$
\frac{dV}{dt} = \frac{1}{\tau} \bigg( V_0-V\bigg) 
$$This has one fixed point at $V=V_0.$
The solution to the system has become exponential now. 
$$
V(t) = e^{(V_0-V)/\tau}
$$
Say the system is at potential $V=v$, then
- If $v<V_0$: exponent is positive. $\implies V$ will grow until it reaches $V_0$
- If $v>V_0$: exponent is negative. $\implies V$ will decay until it reaches $V_0$

## Case-3
To this system we introduce external stimulus as  a constant current, $I$.
$$
\frac{dV}{dt} = \frac{1}{\tau} \bigg( V_0-V+RI\bigg) 
$$

$R$ is the effective resistance. Now no major changes happened, except the fixed point $V_0$ changed to $V_0+RI$, a higher value, assuming the current, $I>0$.

We can also incorporate the current as a function of time , which is equivalent to moving the fixed point up, so that you build up potential to reach the new fixed point.
## Firing
Firing is an externally enforced condition, as it is not something inherently emerging from the model. So we define an arbitrary threshold, say $V_{\epsilon}>V(t)$ and propose, the moment $V = V_{\epsilon}$ , we set $V=V_0$. 

# Remarks
The LIF neuron model is this. 
$$
\dot{x} = \tau(a-x)
$$
- $\tau$ is the rate, which determines the timescale($\tau^{-1}$)
- $a$ is the fixed point ( $V_0+RI(t)$ )


# Numeric Simulation
- $E_0$ = -70 mV
- $E_q$ = -55 mV
- $R$ = 1 A
- $\tilde{A} = $
