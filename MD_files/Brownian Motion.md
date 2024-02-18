Robert Brown in 1827, observed the irregular state of motion of small pollen particles suspended in water. After years, there was not a good explanation for this phenomena, until* [[Albert Einstein]]* published the article called
*[[On the Movement of Small Particles Suspended in Stationary Liquids Required by the Molecular-Kinetic Theory of Heat]]*.
Two main assumptions were stated by Einstein
- The motion of the pollen particle is due the frequent impact of the motion of the molecules of liquid in which the particle is suspended.
- The motion of these molecules is so complicated that the effect on the pollen particle can only be described probabilistically.

### Quotes

*It must be clearly be assumed that each individual particle executes a motion which is independent of all other particles; it will also be considered that the movements of one and the same particle in different time intervals are independent processes, as long as the time intervals are not chosen too small*

*We introduce a time interval $\tau$ into consideration, which is very small compared to the observable time intervals, but nevertheless so large that in two successive  time intervals $\tau$, the motions executed by the particle can be thought of as events which are independent of each other*
## Einstein derivation

Let there be a total of $n$ particles suspended in a liquid. In a time interval $\tau$, the $x$ coordinate of the individual particles will increase by an amount ${} \delta {}$. which of each particle ${} \delta {}$ is different and has different value. We can define a frequency law for ${} \delta {}$; the number of particles $dn$ which experience a shift which is between $\delta$ and $\delta+d\delta$ will be expressible by an equation of the form:
$$\begin{align}
dn&=n\phi(\delta)d\delta
\end{align}$$
^freqlaw
where $\int_{\infty}^{\infty}\phi(\delta)d\delta=1$, and $\phi(\delta)=\phi(-\delta)$, and is only different from zero for small values of $\delta$.

We will assume that the number of particles per unit of volume depends only on $x$ and $t$. Let $\nu = f(x,t)$ be the number of particles per unit of volume. We compute the distribution of particle at time $t+\tau$ from the distribution at time $t$. From the definition of the function $\phi(\delta)$, we can find the number of particles which at time $t+\tau$ are found between two planes perpendicular to the $x$-axis and passing through points $x$ and $x+dx$.
$$f(x,t+\tau)dx=dx\int d\delta\ f(x+\delta,t)\phi(\delta)$$
we can expand the left side in powers of $\tau$ up to $O(1)$, since $\tau$ is small
$$f(x,t+\tau)=f(x,t)+\tau\frac{\partial f}{\partial t}$$
And for $\delta$, we can do the same up to whatever order $\delta$ is different to zero, which by definition is for small values of $\delta$
$$f(x+\delta,t)=f(x,t)+\delta\frac{\partial f}{\partial x}+\frac{\delta^2}{2!}\frac{\partial^{2}f}{\partial x^{2}}+\dots$$
Now putting this inside the integral, and using the fact that $\phi$ is a symmetric function the even powers vanish. Defining
$$\frac{1}{2\tau}\int \delta^2\phi(\delta)d\delta=D$$
Keeping only first and third order terms in the right-hand side, we found a one dimensional [[Diffusion equation]] for $f$.

$$\begin{align}
\frac{df}{dt}=D\frac{\partial^2f}{\partial x^2}
\end{align}$$
where $D$ is the [[Diffusion coefficient]], and now neglecting interaction between particles the problem is completely solved with solution

$$f(x,t)= \frac{n}{\sqrt{4\pi D}}\frac{\exp{(-x^{2}/4Dt)}}{\sqrt{t}}$$
