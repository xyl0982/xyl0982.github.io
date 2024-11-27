---
date: '2023-08-04T00:37:31Z'
title: 'Minimal Surface-Isothermal Coordinate System and W-E Representation'
tags: ["Visualization", "Complex Analysis"]
categories: ["Applied Math"]
---

##  Isothermal Coordinate System

In the previous two sections, we have not been able to give a clear definition of minimal surfaces. In this section, we define minimal surfaces, compute their curvature, and find their Gauss map. Let us start with the definition.

#### Definition of Minimal Surface

We say a surface is a **minimal surface** if its mean curvature $H = 0$.

#### Definition of Isothermal Coordinates

Let $r = r(u, v)$ be a regular parametrized surface. We say that $r$ is **isothermal** if:

$$
E = G \quad \text{and} \quad F = 0,
$$

where $E$, $F$, and $G$ are the coefficients of the first fundamental form.

#### Proposition: Conversion to Isothermal Coordinates

Let $r = r(u, v)$ be a regular parametrized surface. There exists a local change of coordinates $(u, v) \to (x, y)$ such that in the new coordinates the surface becomes isothermal. That is, the coefficients of the first fundamental form satisfy $E = G$ and $F = 0$.

#### Proof Sketch

Given a surface $r = r(u, v)$, the first fundamental form is:

$$
I = E \, du^2 + 2F \, du \, dv + G \, dv^2.
$$

To achieve isothermal coordinates, we need:

$$
E \, dx^2 + G \, dy^2 \quad \text{and} \quad F = 0.
$$

This can be done by solving the Beltrami equation for conformal mappings:

$$
\frac{\partial x}{\partial u} \frac{\partial y}{\partial v} + \frac{\partial x}{\partial v} \frac{\partial y}{\partial u} = 0.
$$

Details of the proof involve constructing such coordinates locally using complex analysis.

#### Minimal Surface Equation in Isothermal Coordinates

If $r = r(u, v)$ is an isothermal parametrization of a minimal surface, then $r$ satisfies the equation:

$$
r_{uu} + r_{vv} = 0.
$$

This is equivalent to the condition that the parametrized surface is harmonic.

#### Gauss Map of a Minimal Surface

Let $r = r(u, v)$ be a minimal surface, and let $\mathbf{n}$ be the unit normal vector. The **Gauss map** $N : S \to \mathbb{S}^2$ sends each point $p$ on the surface to the corresponding unit normal vector $\mathbf{n}(p)$.

For minimal surfaces in isothermal coordinates, the Gauss map $N$ satisfies:

$$
N = \frac{r_u \times r_v}{\| r_u \times r_v \|}.
$$

#### Example: Minimal Surfaces in Isothermal Coordinates

1. **Catenoid**: The catenoid can be parametrized in isothermal coordinates as:

   $$
   r(u, v) = (c \cosh(u) \cos(v), c \cosh(u) \sin(v), u).
   $$

2. **Helicoid**: The helicoid can be written as:

   $$
   r(u, v) = (u \cos(v), u \sin(v), c v).
   $$

Both examples demonstrate how isothermal coordinates simplify the representation of minimal surfaces.

#### Conclusion

Isothermal coordinates are a powerful tool for studying minimal surfaces. They simplify the equations governing these surfaces and provide a natural framework for exploring their geometric properties.

## Weierstrass-Enneper Representation of Minimal Surface

With all of this background information about minimal surfaces, isothermal patches, harmonic functions, and holomorphic and meromorphic functions, the Weierstrass-Enneper representation for minimal surfaces may be constructed. Now we start from three complex functions.

For a given surface $r(u,v) = (x(u,v), y(u,v), z(u,v))$, we consider:

$$
\phi_1(w) = \frac{\partial x}{\partial u} - i \frac{\partial x}{\partial v}, \quad
\phi_2(w) = \frac{\partial y}{\partial u} - i \frac{\partial y}{\partial v}, \quad
\phi_3(w) = \frac{\partial z}{\partial u} - i \frac{\partial z}{\partial v},
$$

where $w = u + iv$. Now consider the sum of the square of the three complex functions, then we can get an interesting conclusion connected with the isothermal coordinate.

#### Theorem

For a given surface $r(u,v) = (x(u,v), y(u,v), z(u,v))$, we define:

$$
\phi_1(w) = \frac{\partial x}{\partial u} - i \frac{\partial x}{\partial v}, \quad
\phi_2(w) = \frac{\partial y}{\partial u} - i \frac{\partial y}{\partial v}, \quad
\phi_3(w) = \frac{\partial z}{\partial u} - i \frac{\partial z}{\partial v}.
$$

The surface $r$ is an isothermal coordinate system if and only if $\phi_1(w)$, $\phi_2(w)$, $\phi_3(w)$ are holomorphic and satisfy:

$$
\phi_1^2(w) + \phi_2^2(w) + \phi_3^2(w) = 0.
$$

When we study a minimal surface, the case where all of $\phi_1(w)$, $\phi_2(w)$, $\phi_3(w)$ are identically zero is excluded because it gives no surface. Hence we assume that $\phi_3$ is not identically zero. If we define:

$$
f = \phi_1 - i\phi_2, \quad g = \frac{\phi_3}{\phi_1 - i\phi_2},
$$

then $f$ is a holomorphic function and $g$ is a meromorphic function, since:

$$
\phi_1^2(w) + \phi_2^2(w) + \phi_3^2(w) = 0 \implies \phi_1 + i\phi_2 = -\frac{\phi_3^2}{\phi_1 - i\phi_2} = -fg^2.
$$

Then we obtain:

$$
\phi_1 = \frac{1}{2}f(1 - g^2), \quad
\phi_2 = \frac{i}{2}f(1 + g^2), \quad
\phi_3 = fg.
$$

#### Theorem

A simply connected minimal surface is expressed as the following:

$$
r(w) = \left(
\text{Re} \int_0^w \frac{1}{2}f(1 - g^2) \, dw,
\text{Re} \int_0^w \frac{i}{2}f(1 + g^2) \, dw,
\text{Re} \int_0^w fg \, dw
\right), \quad w \in D,
$$

where $D$ is the unit open disk:

$$
\{w \in \mathbb{C} \mid |w| < 1\}
$$

or the total plane $\mathbb{C}$, $f(w)$ is a holomorphic function on $D$, and $g(w)$ is a meromorphic function on $D$.

#### Example (Enneper’s Surface)

Let $D = \mathbb{C}$, $w = u + iv$, $f(w) = 2$, $g(w) = w$. Then we have:

$$
x = \text{Re} \int_0^w (1 - w^2) \, dw = \text{Re}(w - \frac{1}{3}w^3) = u + uv^2 - \frac{1}{3}u^3,
$$

$$
y = \text{Re} \int_0^w i(1 + w^2) \, dw = \text{Re}(i(w + \frac{1}{3}w^3)) = -v - u^2v + \frac{1}{3}v^3,
$$

$$
z = \text{Re} \int_0^w 2w \, dw = \text{Re}(w^2) = u^2 - v^2.
$$


