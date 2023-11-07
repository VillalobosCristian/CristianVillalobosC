	


## Experiments XY plane. 

### Spring Model
We used an [[Overdamped Langevin equation]] to describe the droplet's motion in the presence of the bacterial bath and subjected to spherical confinement. We consider as a first approximation that the inner droplet is a passive particle trapped in a harmonic potential subjected to an [[active noise]] due to the bacterial suspension. The outer droplet's confinement can be considered a harmonic potential for small displacement. This approximation gives us an analytical expression that describes the functional form of the mean square displacement from the experimental data. This model has been used previously in  [[@Generalized Energy Equipartition in Harmonic Oscillators Driven by Active Baths]]

$$\begin{equation}
	\dot{x}=u(t)-\frac{1}{\tilde{\tau}} x,
\end{equation} $$
Where $\tilde{\tau}=\Gamma/k$, with $\Gamma=6\pi\eta r_i$ the friction coefficient, $k$ the spring constant for the harmonic potential, and $u(t)$ is the active noise induced by the bacterial suspension. We will model the active noise as a colored Gaussian noise with the following statistical properties:
$$ \begin{align}

     \langle u(t)\rangle &=0,\\
     \langle u(t)u(t')\rangle &=v^2_b e^{-|t-t'|/\tau}.
 \end{align}$$
The solution of equation \ref{eq.langevin_spring_model} is given by:
$$\begin{equation}

	x(t)  = \int_{-\infty}^{t}e^{-\frac{1}{\tilde{\tau}}(t-s)}u(s)\, d s,
\end{equation}$$
Here we use the fact that as the particle is confined, the integral can be done from minus infinity without divergences. The mean square displacement is found to be:
$$\begin{align}

    \langle  \Delta x^2(t) \rangle &=  \frac{2v_b^2 \tilde{\tau}^2 \tau \left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}})\right)}{\tilde{\tau}^2 - \tau^2}.
\end{align}$$
I will present the mean squared displacement (MSD) results for each Double Emulsion experiment, fitting the MSD equation.
As t approaches infinity, the exponential terms go to zero. Thus the expression simplifies to:

$$\langle  \Delta r_i^2(t) \rangle =4v_b^2\tau(\tilde{\tau}-\tau)\frac{\tilde{\tau}^2}{(\tilde{\tau}+\tau)(\tilde{\tau}-\tau)}=\frac{4v_b^2\tau\tilde{\tau}^2}{\tilde{\tau}+\tau}$$
Now is $t\to 0$

$$\lim_{t\to0} \langle  \Delta r_i^2(t) \rangle =  2\frac{v_b^2t^2\tilde{\tau}}{\tau+\tilde{\tau}}$$

The MSD equation involves three parameters, namely $\tau$, $\tilde{\tau}$, and $v_b$, which we aim to determine. To simplify the fitting procedure, we can express the equation in an alternative form.





$$\begin{align}
    \langle  \Delta r_i^2(t) \rangle &=  \frac{4v_b^2 \tilde{\tau}^2 \tau \left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}})\right)}{\tilde{\tau}^2 - \tau^2}.\\
    \langle  \Delta r_i^2(t) \rangle &= \frac{4v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}}) \right).
\end{align}$$
If we expand the exponential term involving $\tilde{\tau}$, assuming that $\tilde{\tau }\gg t$, we have:
$$\begin{align}
    \langle  \Delta r_i^2(t) \rangle &=  \frac{4v_b^2 \tilde{\tau}^2 \tau \left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}})\right)}{\tilde{\tau}^2 - \tau^2}.\\
    \langle  \Delta r_i^2(t) \rangle &= \frac{4v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(\tilde{\tau}(1 - (1-\frac{t}{\tilde{\tau}}+ \frac{t^2}{2\tilde{\tau}^{2}})) - \tau(1 - e^{-\frac{t}{\tau}}) \right),\\
    
     \langle  \Delta r_i^2(t) \rangle &= \frac{4v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(\tilde{\tau}(1 - 1+\frac{t}{\tilde{\tau}}- \frac{t^2}{2\tilde{\tau}^{2}})) - \tau(1 - e^{-\frac{t}{\tau}}) \right),\\
       \langle  \Delta r_i^2(t) \rangle &= \frac{4v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(t- \frac{t^2}{2\tilde{\tau}} - \tau(1 - e^{-\frac{t}{\tau}}) \right)
\end{align}$$


$$\begin{align*}
\langle  \Delta r_i^2(t) \rangle &= \frac{4v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(\frac{2t\tilde{\tau}-t^2-2\tau\tilde{\tau}(1-e^{-t/\tau})}{2\tilde{\tau}}\right)\\
\langle  \Delta r_i^2(t) \rangle &= \frac{2v_b^2\tilde{\tau}\tau}{{\tilde{\tau}^2 - \tau^2}}\left(2t\tilde{\tau}-t^2-2\tau\tilde{\tau}(1-e^{-t/\tau})\right),\\
\langle  \Delta r_i^2(t) \rangle &= \frac{2v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(2t-\cancel{\frac{t^2}{\tilde{\tau}}}-2\tau(1-e^{-t/\tau})\right)
\end{align*}$$
Defining 
$$V^{2}=\frac{v_b^2\tilde{\tau}^{2}}{\tilde{\tau}^{2}-\tau^{2}}$$
$$\begin{align*}
\langle  \Delta r_i^2(t) \rangle &= 4V^2\tau\left(t-\tau(1-e^{-t/\tau})\right)
\end{align*}$$
Which only depend on two parameters. 

In terms of this definition for $V^2$  we have at short time $t\to 0$:

$$\begin{align}
    \langle  \Delta r_i^2(t) \rangle &=  4V^2\tau \left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}})\right).\\
    \langle  \Delta r_i^2(t) \rangle &= \frac{4v_b^2\tilde{\tau}^2\tau}{{\tilde{\tau}^2 - \tau^2}}\left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}}) \right).
\end{align}$$

$$\begin{align*}
 \langle  \Delta r_i^2(t) \rangle &= 4V^2\tau\left(\tilde{\tau}(1 - (1-\frac{t}{\tilde{\tau}}+ \frac{t^2}{2\tilde{\tau}^{2}})) - \tau(1 - (1-\frac{t}{\tau}+\frac{t^2}{2\tau^2})) \right),\\
\langle  \Delta r_i^{2}(t) \rangle &= V^2\tau\left(\frac{2t^2(\tilde{\tau}-\tau)}{\tilde{\tau}\tau}\right),\\
\langle \Delta r^{2}_{i}\rangle &= \frac{2V^2(\tilde{\tau}-\tau)}{\tilde{\tau}}.\\
\langle \Delta r^{2}_{i}\rangle &= 2\frac{v_b^2\tilde{\tau}^{2}}{\tilde{\tau}^{2}-\tau^{2}}\frac{(\tilde{\tau}-\tau)}{\tilde{\tau}}=\frac{2v_b^2\tilde{\tau}}{\tilde{\tau}+\tau}.\\
\end{align*}$$
---
For $t\to \infty$
$$\begin{align}
    \langle  \Delta r_i^2(t) \rangle &=  4V^2\tau \left(\tilde{\tau}(1 - e^{-\frac{t}{\tilde{\tau}}}) - \tau(1 - e^{-\frac{t}{\tau}})\right).\\
    \langle  \Delta r_i^2(t) \rangle &= 4V^2\tau(\tilde{\tau}-\tau).\\
\langle  \Delta r_i^2(t) \rangle &=4v_b^2\tau(\tilde{\tau}-\tau)\frac{\tilde{\tau}^2}{(\tilde{\tau}+\tau)(\tilde{\tau}-\tau)}=\frac{4v_b^2\tau\tilde{\tau}^2}{\tilde{\tau}+\tau}
\end{align}$$


