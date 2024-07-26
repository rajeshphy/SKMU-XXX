---
layout: post
title:  "Approximation Method"
date:   2024-07-26 10:47:26 +0530
categories: lecture
---

### Time Independent Perturbation Theory: Non-degenerate Case

Suppose we have a Hamiltonian 

$$H = H_0 + \lambda H'$$

where $$\lambda$$ is a small parameter. The Hamiltonian $$H_0$$ is the unperturbed Hamiltonian whose eigenvalues and eigenfunctions are known say $$E_n^{(0)}$$ and $$\psi_n^{(0)}$$ respectively. The Hamiltonian $$H'$$ is the perturbation to the Hamiltonian $$H_0$$. Now the problem is <span style="color: red; font-weight: bold;">to find the eigenvalues and eigenfunctions of the Hamiltonian $$H$$.</span>

- If the unperturbed Hamiltonian $$H_0$$ is known, then the eigenvalues and eigenfunctions of $$H$$ can be found by using perturbation theory.
- The eigenvalues and eigenfunctions of $$H$$ can be expanded in powers of $$\lambda$$.
- The eigenvalues of $$H$$ are given by:

    $$E_n = E_n^{(0)} + \lambda E_n^{(1)} + \lambda^2 E_n^{(2)} + \cdots$$

    where $$E_n^{(0)}$$ are the eigenvalues of $$H_0$$ and $$E_n^{(1)}$$ are the first order corrections to the eigenvalues. Similarly, $$E_n^{(2)}$$ are the second order corrections to the eigenvalues.

- The eigenfunctions of $$H$$ are given by:

    $$\psi_n = \psi_n^{(0)} + \lambda \psi_n^{(1)} + \lambda^2 \psi_n^{(2)} + \cdots$$

    where $$\psi_n^{(0)}$$ are the eigenfunctions of $$H_0$$ and $$\psi_n^{(1)}$$ are the first order corrections to the eigenfunctions. Similarly, $$\psi_n^{(2)}$$ are the second order corrections to the eigenfunctions.

- The first order correction to the eigenvalues is given by:

    $$E_n^{(1)} = \int \psi_n^{(0)*} H' \psi_n^{(0)} \, d\tau$$

    One gets this by substituting the above expression for $$E_n$$ into the Schrödinger equation and then projecting the equation onto $$\psi_n^{(0)}$$. We will use the fact that 

    $$\int \psi_n^{(0)*} \psi_n \, d\tau = \int \psi_n^{(0)*} \psi_n^{(0)} \, d\tau = 1$$ 
    
    Expanding the Schrödinger equation gives

    $$\begin{align}
    \int \psi_n^{(0)*} (H_0 + \lambda H') \psi_n \, d\tau &= E_n \int \psi_n^{(0)*} \psi_n \, d\tau\\
    \int \psi_n^{(0)*} H_0 \psi_n \, d\tau + \lambda \int \psi_n^{(0)*} H' \psi_n \, d\tau &= E_n \int \psi_n^{(0)*} \psi_n^{(0)} \, d\tau\\
    E_n^{(0)} \int \psi_n^{(0)*} \psi_n \, d\tau + \lambda \int \psi_n^{(0)*} H' \psi_n \, d\tau &= E_n \\
    E_n^{(0)} \int \psi_n^{(0)*} \psi_n^{(0)} \, d\tau + \lambda \int \psi_n^{(0)*} H' \psi_n \, d\tau &= E_n^{(0)}+ \lambda E_n^{(1)}+ \lambda^2 E_n^{(2)} + \cdots\\
    E_n^{(0)}+ \lambda \int \psi_n^{(0)*} H' \psi_n \, d\tau &= E_n^{(0)}+ \lambda E_n^{(1)}+ \lambda^2 E_n^{(2)} + \cdots\\
    \lambda \int \psi_n^{(0)*} H' \psi_n \, d\tau &= \lambda E_n^{(1)}+ \lambda^2 E_n^{(2)} + \cdots
    \end{align}$$

    Expanding the perturbative term on L.H.S. of the above equation gives

    $$\int \psi_n^{(0)*} H' \psi_n \, d\tau =\int \psi_n^{(0)*} H' \psi_n^{(0)} \, d\tau+ \lambda\int \psi_n^{(0)*} H' \psi_n^{(1)} \, d\tau+ \lambda^2\int \psi_n^{(0)*} H' \psi_n^{(2)} \, d\tau+ \cdots$$
    
    therefore the Schrödinger equation gives

    <span style="color: red; font-weight: bold;">$$\lambda\int \psi_n^{(0)*} H' \psi_n^{(0)} \, d\tau+ \lambda^2\int \psi_n^{(0)*} H' \psi_n^{(1)} \, d\tau+ \cdots=\lambda E_n^{(1)}+ \lambda^2 E_n^{(2)} + \cdots$$</span>

    we get first order corrections to the eigenvalues as

    $$\boxed{E_n^{(1)} = \int \psi_n^{(0)*} H' \psi_n^{(0)} \, d\tau}$$

    First order correction can be calculated as the expression of the eigenfunction $$\psi_n^{(0)}$$ is well known and the matrix element of $$H'$$ can be calculated. The second order correction to the eigenvalues is given by:

    $$\boxed{E_n^{(2)} = \int \psi_n^{(0)*} H' \psi_n^{(1)} \, d\tau}$$

    Here the first order correction to the eigenfunction is needed to calculate the second order correction to the eigenvalues.

- The first order correction to the eigenfunctions is given by:

    $$\psi_n^{(1)} = \sum_{m \neq n} \frac{\psi_m^{(0)*} H' \psi_n^{(0)}}{E_n^{(0)} - E_m^{(0)}}$$

    The first order correction to the eigenfunction can be calculated by using the fact that the eigenfunctions of $$H_0$$ are known and the matrix elements of $$H'$$ can be calculated. The first order correction to the eigenfunction is calculated by projecting the Schrödinger equation onto the state $$\psi_m^{(0)}$$ where $$m \neq n$$.