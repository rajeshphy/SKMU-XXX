---
layout: post
title:  "Scattering"
date:   2024-07-12 10:47:26 +0530
categories: lecture
---
<img src="/SKMU/assets/img/Quantum/Scattering.jpeg" alt="Interaction Process" class="my-custom-class" style="max-width:100%; height:auto;">

Consider time-independent scattering theory, for which the Hamiltonian, $$H$$, of the system is given by

$$ H=H_o+H_1$$

where, $$H_0$$ is the Hamiltonian of a free particle with eigenfunction

$$\phi(\mathbf{x})=e^{i\mathbf{k\cdot x}}$$

and $$H_1$$ is the scattering source. The Schrödinger equation for the system at point $$\mathbf{x}$$ is given by

$$ H\psi(\mathbf{x})=E\psi(\mathbf{x})$$

where, $$E$$ is the energy of the system and considering the scattering to be elastic the energy of the system is conserved. Therefore $$E$$ is same as the energy possessed by the incident plane wave with wavevector $$k$$ before scattering. The Schrödinger equation therefore reduces to

$$\begin{align}(H_o+H_1)\psi(\mathbf{x})&=E\psi(\mathbf{x})\\\left(-\frac{\hbar^2}{2m}\nabla^2+H_1\right)\psi(\mathbf{x})&=\frac{\hbar^2 k^2}{2m}\psi(\mathbf{x})\\ \left(-\nabla^2+V\right)\psi(\mathbf{x})&=k^2\psi(\mathbf{x}) \qquad \text{Dividing throughout by }\hbar^2/2m \\ \left(\nabla^2+k^2\right)\psi(\mathbf{x})&=V(\mathbf{x})\psi(\mathbf{x}) \qquad \text{where, } V(\mathbf{x})=2mH_1/\hbar^2\end{align}$$

The above equation is the Helmholtz equation and the green's function for the Helmholtz equation is given by

$$ G(\mathbf{x},\mathbf{x'})=-\frac{1}{4\pi}\frac{e^{ik'|\mathbf{x}-\mathbf{x'}|}}{|\mathbf{x}-\mathbf{x'}|}$$

The solution to the Helmholtz equation is given by

$$\begin{align} \psi(\mathbf{x})&=-\frac{1}{4\pi}\int d^3x' G(\mathbf{x},\mathbf{x'})V(\mathbf{x'})\psi(\mathbf{x'})\\
&= -\frac{1}{4\pi}\int d^3x' \frac{e^{ik'|\mathbf{x}-\mathbf{x'}|}}{|\mathbf{x}-\mathbf{x'}|}V(\mathbf{x'})\psi(\mathbf{x'})\end{align}$$

We add a term $$\phi(\mathbf{x})$$ to the above equation to account for the incident wave. The distance $$\|\mathbf{x}-\mathbf{x'}\|$$ for large distance from the scattering source is approximated to $$(x-\mathbf{\hat{n}\cdot x'})=(r-x'\cos \alpha)$$, where $$\mathbf{\hat{n}}$$ is the unit vector in the direction of $$\mathbf{x}$$. The denominator will be approximated by $$r$$. 

$$\begin{align}\psi(\mathbf{x})&=\phi(x)-\frac{1}{4\pi}\int d^3x' \frac{e^{ik'(r-x'\cos\alpha)}}{r}V(\mathbf{x'})\psi(\mathbf{x'})\\
&=\phi(x)-\left[\frac{1}{4\pi}\int d^3x' e^{-ik' x'\cos \alpha}\;V(\mathbf{x'})\psi(\mathbf{x'})\right]\frac{e^{ik'r}}{r}\end{align}$$

Since the collision is elastic so the scattered wave has the same energy as the incident wave and therefore the magnitude of <script type="math/tex">|\mathbf{k}|=|\mathbf{k'}|=k</script>. Therefore the solution to the Helmholtz equation is given by

$$\begin{align} \psi(\mathbf{x})&=\phi(\mathbf{x})+f(\mathbf{k',k})\frac{e^{ikr}}{r}\\ f(\mathbf{k',k})&=-\frac{1}{4\pi}\int d^3x' e^{-ik' x'\cos \alpha}V(\mathbf{x'})\psi(\mathbf{x'})\end{align}$$

The function $$f(\mathbf{k',k})$$ is called the scattering amplitude. The differential scattering cross-section is given by

$$\frac{d\sigma}{d\Omega}=|f(\mathbf{k',k})|{}^2$$

The total scattering cross-section is given by

$$\sigma_{\text{total}}=\int |f(\mathbf{k',k})|^2 d\Omega$$

## Born Approximation

The Born approximation is a method used to solve the scattering amplitude, $$f(\mathbf{k',k})$$, for a given small potential $$V(\mathbf{x})$$ by approximating the wavefunction $$\psi(\mathbf{x})$$ with the incident wavefunction $$\phi(\mathbf{x})$$ as

$$\begin{align} f(\mathbf{k',k})&=-\frac{1}{4\pi}\int d^3x' e^{-ik' x'\cos \alpha}V(\mathbf{x'})\phi(\mathbf{x'})\\
&= -\frac{1}{4\pi}\int d^3x' e^{-i\mathbf{k'\cdot x'}}V(\mathbf{x'})e^{i\mathbf{k\cdot x'}}\\
&=-\frac{1}{4\pi}\int d^3x' e^{i\mathbf{(k-k')\cdot x'}}V(\mathbf{x'})\end{align}$$





### Scattering Amplitude $$f(k',k)$$ simplification for a Spherically Symmetric Potential

Consider a spherically symmetric potential $$V(\mathbf{x})=V(r)$$, where <script type="math/tex">
r = |\mathbf{x}|
</script>. The integration of scattering amplitude can be simplified by choosing a new $$z$$-axis along the direction of the vector $$\mathbf{q=k-k'}$$, so that $$\mathbf{(k-k')\cdot x'}=q r' \cos \theta'$$, where <script type="math/tex">r'=|\mathbf{x'}|</script>.

$$\begin{align} f(k',k)&=-\frac{1}{4\pi}\int d^3x' e^{i\mathbf{(k-k')\cdot x'}}V(\mathbf{x'})\\
&=-\frac{1}{4\pi}\int_0^\infty dr' r'^2 \int_0^\pi d\theta' \sin \theta' \int_0^{2\pi} d\phi' e^{iqr'\cos \theta'}V(r')\\
&=-\frac{1}{4\pi}\int_0^\infty dr' r'^2 \int_0^\pi d\theta' \sin \theta'e^{iqr'\cos \theta'} \int_0^{2\pi} d\phi' V(r')\\
&=-\frac{1}{4\pi}\int_0^\infty dr' r'^2 \int_0^\pi d\theta' \sin \theta'e^{iqr'\cos \theta'}\cdot 2\pi\cdot V(r')\\
&=-\frac{1}{4\pi}\int_0^\infty dr' r'^2 \cdot 2\frac{\sin qr'}{qr'}\cdot 2\pi\cdot V(r')\\
&=-\int_0^\infty dr' r'^2 \frac{\sin qr'}{qr'} V(r')\\
&=-\frac{1}{q}\int_0^\infty r'\sin qr'V(r')dr'
\end{align}$$

The value of $$q$$ in terms of wavevector $$k$$ and $$k'$$ is given by

$$q=2k\cos\frac{\theta}{2}$$

as depicted in figure below.

<img src="/SKMU/assets/img/Quantum/Scattering-Angle.png" alt="Interaction Process" class="my-custom-class" style="max-width:100%; height:auto;">

Therefore the scattering amplitude for a spherically symmetric potential obtained by replacing $$V(r)$$ with $$\frac{2m}{\hbar^2}H_1$$ is given by

$$f(k',k)=-\frac{2m}{\hbar^2q}\int_0^\infty r'\sin qr'H_1dr'$$

### Scattering by a soft sphere

Consider a soft sphere potential given by

$$H_1=\begin{cases} V_0 & \text{for } r<R\\ 0 & \text{for } r>R \end{cases}$$

here the constant $$V_0$$ is finite as Born approximation is valid for small potentials. The scattering amplitude for the soft sphere potential is given by

$$\begin{align}f(k',k)&=-\frac{2m}{\hbar^2q}\int_0^R r'\sin qr'V_0dr'\\
&=-\frac{2mV_0}{\hbar^2q}\int_0^R r'\sin qr'dr'\\
&= -\frac{2mV_0}{\hbar^2q}\left[\frac{\sin (q R)-q R \cos (q R)}{q^2}\right]\\
&= \frac{2mV_0}{\hbar^2q^3}\left[q R \cos (q R)-\sin (q R)\right]\end{align}$$

---
# Rutherford Scattering

The static screened Coulomb potential of an atomic nucleus (also called Yukawa potential) has the form 

$$H_1=\beta \frac{e^{-\mu r}}{r}$$

where, $$\beta$$ is the strength of the potential, $$\mu$$ is the range of the potential and $$r$$ is the distance from the nucleus. The scattering amplitude for the Rutherford scattering under Born approximation is given by

$$\begin{align}f(k',k)&=-\frac{2m}{\hbar^2q}\int_0^\infty r'\sin qr'\beta \frac{e^{-\mu r'}}{r'}dr'\\
&=-\frac{2m\beta}{\hbar^2q}\int_0^\infty \sin qr' e^{-\mu r'}dr'\\
&= -\frac{2m\beta}{\hbar^2q}\left[\frac{q}{\mu ^2+q^2}\right]\\
&= -\frac{2m\beta}{\hbar^2}\frac{1}{\mu ^2+q^2}\end{align}$$


The differential scattering cross-section for Rutherford scattering is given in the limit $$\mu \rightarrow 0$$ as

$$\frac{d\sigma}{d\Omega}=\left(\frac{2m\beta}{\hbar^2q^2}\right)^2$$

We can replace $$q$$ in terms of $$k$$ as $$q=2k\sin \frac{\theta}{2}$$, where $$\theta$$ is the scattering angle. Therefore the differential scattering cross-section for Rutherford scattering is given by

$$\frac{d\sigma}{d\Omega}=\left(\frac{m\beta}{\hbar^2}\right)^2\frac{1}{4k^4\sin^4\frac{\theta}{2}}$$

Since the kinetic energy of the incident particle is $$E=\frac{\hbar^2 k^2}{2m}$$, the differential scattering cross-section can be written in terms of the kinetic energy as

$$\frac{d\sigma}{d\Omega}=\left(\frac{\beta}{4E}\right)^2\frac{1}{\sin^4\frac{\theta}{2}}$$

Which is the Rutherford scattering formula as derived by Rutherford in 1911 classically.

---
# Partial Wave Analysis and Phase Shifts

The incident plane wave 

$$\phi(\mathbf{x})=e^{i\mathbf{k\cdot x}}$$

can be expanded in terms of spherical harmonics $$Y_{lm}(\theta,\phi)$$ as

$$\begin{align}e^{i\mathbf{k\cdot x}}&=\sum_{l=0}^\infty \sum_{m=-l}^l C_{lm}\; j_l(kr)Y_{lm}(\theta,\phi)\end{align}$$

where, $$j_l(kr)$$ is the spherical Bessel function of the first kind and $$C_{lm}$$ is the constant. Since a plane wave is symmetric in $$\phi$$ coordinate and therefore it is independent of $$m$$, further at large distances from the scattering source, the behavior of the spherical Bessel function is approximated as

$$\begin{align}j_l(kr)&\approx \frac{\sin(kr-l\pi/2)}{kr}\\
&=\frac{1}{2ikr}\left[e^{i(kr-l\pi/2)}-e^{-i(kr-l\pi/2)}\right]
\end{align}$$

therefore the incident plane wave can be written as

$$\begin{align}e^{i\mathbf{k\cdot x}}&=\sum_{l=0}^\infty C_l \; j_l(kr)P_l(\cos \theta)\\
&=\sum_{l=0}^\infty\;C_l\; j_l(kr)P_l(\cos \theta)\\&=\frac{1}{2ik}\sum_{l=0}^\infty \;C_l\left[\frac{e^{i(kr-l\pi/2)}}{r}-\frac{e^{-i(kr-l\pi/2)}}{r}\right]P_l(\cos \theta)
\end{align}$$

where, $$P_l(\cos \theta)$$ is the Legendre polynomial of degree $$l$$ and $$C_l=(2l+1)\;i^l$$.

The scattering wavefunction $$\psi(\mathbf{x})$$ can then rewritten in terms of summation of partial waves as

$$\begin{align}\psi(\mathbf{x})&= \psi(\mathbf{x})\\
&=e^{i\mathbf{k\cdot x}}+f(\mathbf{k',k})\frac{e^{ikr}}{r}\\
&=\frac{1}{2ik}\sum_{l=0}^\infty \;C_l\left[\frac{e^{i(kr-l\pi/2)}}{r}-\frac{e^{-i(kr-l\pi/2)}}{r}\right]P_l(\cos \theta)+ f(\mathbf{k',k})\frac{e^{ikr}}{r}\\
\end{align}$$

We will use the fact that the amplitude of incoming wave is the same as the amplitude of outgoing wave at large distances from the scattering source. Therefore the above equation can be written as summation over two terms by doing phase shifts of outgoing waves inside the summation to incorporate the outgoing term $$f(\mathbf{k',k})\frac{e^{ikr}}{r}$$ as

$$\begin{align}\psi(\mathbf{x})&=\frac{1}{2ik}\sum_{l=0}^\infty \;C_l\left[\frac{e^{i(kr-l\pi/2)+2i\delta_l}}{r}-\frac{e^{-i(kr-l\pi/2)}}{r}\right]P_l(\cos \theta)\\
&=\frac{1}{2ik}\sum_{l=0}^\infty \;C_l\left[\frac{e^{ikr}}{r}e^{i(2\delta_l-l\pi/2)}-\frac{e^{-i(kr-l\pi/2)}}{r}\right]P_l(\cos \theta)\\
&=\frac{1}{2ik}\sum_{l=0}^\infty \;C_l\left[\frac{e^{ikr}}{r}(-i)^le^{i2\delta_l}-\frac{e^{-i(kr-l\pi/2)}}{r}\right]P_l(\cos \theta)\\
\end{align}$$

where, $$\delta_l$$ is the phase shift for the $$l$$-th partial wave. The scattering amplitude $$f(\mathbf{k',k})=f(\theta)$$ can therefore be calculated from two successive results by comparing the factor of $$\frac{e^{ikr}}{r}$$ as

$$\begin{align}f(\theta)&= \frac{1}{2ik}\sum_{l=0}^\infty \;C_l\;(-i)^l\left[e^{i2\delta_l}-1\right]P_l(\cos \theta)\\
&= \frac{1}{k}\sum_{l=0}^\infty \;C_l\;(-i)^l\;\frac{e^{i2\delta_l}-1}{2i}P_l(\cos \theta)\\
&= \frac{1}{k}\sum_{l=0}^\infty \;C_l\;(-i)^l\;\sin \delta_l\;e^{i\delta_l}P_l(\cos \theta)\\
&=\frac{1}{k}\sum_{l=0}^\infty \;(2l+1)\;(-i)^{2l}\;\sin \delta_l\;e^{i\delta_l}P_l(\cos \theta)\\
&=\frac{1}{k}\sum_{l=0}^\infty \;(2l+1)\;\sin \delta_l\;e^{i\delta_l}P_l(\cos \theta)\\
\end{align}$$


Therefore the differential scattering cross-section is given by

$$\frac{d\sigma}{d\Omega}=\left| \frac{1}{k} \sum_{l=0}^\infty \;(2l+1)\;\sin \delta_l\;e^{i\delta_l}P_l(\cos \theta)\right|{}^2$$