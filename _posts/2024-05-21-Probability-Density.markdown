---
layout: post
title:  "Derivations-QM"
date:   2024-07-03 18:47:26 +0530
categories: lecture
---
# Current Density Conservation Equation

The Dirac equation for a free particle is given by:

$$ (i \gamma^\mu \partial_\mu - m) \psi = 0 $$

where $$ \psi $$ is the Dirac spinor, $$ \gamma^\mu $$ are the gamma matrices, $$ \partial_\mu $$ denotes the four-gradient, and $$ m $$ is the mass of the particle. The conjugate of the Dirac spinor $$ \psi $$ is denoted by $$ \bar{\psi} = \psi^\dagger \gamma^0 $$.

## Step-by-Step Derivation

1. **Start with the Dirac Equation:**

   $$ (i \gamma^\mu \partial_\mu - m) \psi = 0 $$

2. **Multiply from the left by $$ \bar{\psi} $$:**

   $$ \bar{\psi} (i \gamma^\mu \partial_\mu - m) \psi = 0 $$

   This expands to:

   $$ i \bar{\psi} \gamma^\mu \partial_\mu \psi - m \bar{\psi} \psi = 0 $$

3. **Take the Dirac conjugate of the Dirac equation:**

   The Dirac conjugate of the Dirac equation is:

   $$ \psi^{\dagger} ( -i \overleftarrow{\partial_\mu} \gamma^{\mu\;\dagger} - m) = 0 $$

   Here, $$ \overleftarrow{\partial_\mu} $$ indicates that the derivative acts to the left. Multiplying both sides by $$\gamma^0$$ on R.H.S we get
   
   $$ \psi^{\dagger} ( -i \overleftarrow{\partial_t} \gamma^{0\;\dagger} -i \overleftarrow{\partial_k} \gamma^{k\;\dagger} - m)\gamma^0 = 0 $$

   and using the property $$\gamma^{k \dagger}=-\gamma^{k}$$ and $$\gamma^0 \gamma^k=\gamma^k\gamma^0$$ and $k\neq0$ we get
   
   $$ \psi^{\dagger} ( -i \overleftarrow{\partial_t} \gamma^{0}\gamma^0 -i \overleftarrow{\partial_k} \gamma^0\gamma^{k} - m\gamma^0) = 0 $$
   
   Now using $$\psi^{\dagger}\overleftarrow{\partial_t} \gamma^0=\partial_t\bar{\psi}$$ we get

   $$ -i \partial_t\bar{\psi} \gamma^0 -i \partial_k\bar{\psi} \gamma^k - m\bar{\psi}  = 0 $$

   In einstein summation form we get

   $$ -i \partial_\mu\bar{\psi} \;\gamma^\mu - m\bar{\psi}  = 0 $$
   
   Multiplying by $$\psi$$ on R.H.S and cancelling negative sign we get

   $$ i \partial_\mu\bar{\psi} \;\gamma^\mu\psi + m\bar{\psi}\psi  = 0 $$

4. **Combine the results:**

   From steps 2 and 3, we have:

   $$ i \bar{\psi} \gamma^\mu \partial_\mu \psi = m \bar{\psi} \psi $$

   And:

   $$ i\partial_\mu \bar{\psi} \gamma^\mu \psi = - m \bar{\psi} \psi $$

6. **Add the conjugate equation from the original:**

   $$ i \bar{\psi} \gamma^\mu \partial_\mu \psi + \partial_\mu \bar{\psi} \gamma^\mu \psi = 0 $$

   This simplifies to:

   $$ i \partial_\mu (\bar{\psi} \gamma^\mu \psi) = 0 $$

7. **Define the current density $$ j^\mu $$:**

   The current density $$ j^\mu $$ is defined as:

   $$ j^\mu = \bar{\psi} \gamma^\mu \psi $$

   Hence, the above equation becomes:

   $$ \partial_\mu j^\mu = 0 $$

## Conclusion

The current density conservation equation derived from the Dirac equation is:

$$ \partial_\mu j^\mu = 0 $$

This equation expresses the conservation of probability current in relativistic quantum mechanics. The four-current $$ j^\mu = \bar{\psi} \gamma^\mu \psi $$ is conserved, indicating that the total probability (or charge) is conserved in the system.