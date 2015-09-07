Introduction and Maps I
=======================

Nonlinearity and Chaos
----------------------

Nonlinear systems are abundant in nature. Most systems show nonlinear dynamics, and most
of those are chaotic.

Systems
-------

###Maps

> *discrete* time, eg. monthly econimic inidators or movie frames.  
> Modeled using **difference equation**

###Flows

> *continous* time, eg. evolution of double pendulum.  
> Modeled using **differential equation**

Difference Equation
-------------------

General form:

$$
x_{n+1} = f(x_n)
$$

###Examples

####Cosine Map

$$
x_{n+1} = cos(x_n)
$$

![Cosine Map for 15 iterations with $$x_n = 1$$. (Code)[#code-cosine-map]](plots/cosine-map.png)


####Logistic Map

$$
x_{n+1} = L(x_n) = R x_n (1 - x_n)
$$

* $$L(x_n)$$: Logistic map function, $$L: [0, 1] \rightarrow [0, 1]$$  
  **Remark**: Maps the unit interval to itself
* $$x$$: state, $$x \in [0, 1]$$
* $$n$$: time, $$n \in \mathbb Z^+$$
* $$R$$: parameter, $$R \in [0, 4]$$

![Logistic map for 60 iterations for various values of $$R \in [0.1, 4.0]$$. (Code)[#code-logistic-map]](plots/logistic-map-contour.png)
![Fixed points for the previous plots with varying values of $$R$$, with $$\varepsilon = 10^{-3}$$. (Code)[#code-logistic-map]](plots/logistic-map-fixedpoints.png)

Code
----

###Code: Cosine Map

[include](cosine-map.jl)

###Code: Logistic Map

[include](logistic-map.jl)
