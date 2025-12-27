# FEM vs Least-Squares FEM

**Dr.-Ing. Serdar Serdas**

Classical FEM has problems with:
- Oscillations in advection
- Stokes/NS pressure-velocity coupling

**LSFEM fixes this**:
$$F(u_h) = \parallel \mathcal{L} u_h - f \parallel^2_0 \quad \rightarrow \quad \mathbf{A}_{SPD} \mathbf{u} = \mathbf{b}$$

**Comparison plan**:
1. Poisson
2. Advection-diffusion-reaction 
3. Stokes
4. Navier-Stokes
5. Porous media
6. FSI
7. PINNs
