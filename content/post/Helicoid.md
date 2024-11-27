---
date: '2023-07-28T00:37:31Z'
title: 'Minimal Surface-Helicoid and Catenoid'
tags: ["Visualization", "Complex Analysis"]
categories: ["Applied Math"]
---

It is easy to see that the equation for a minimal surface is a partial differential equation. In this section, an attempt will be made to find its two famous special solutions: the **catenoid** and the **helicoid**.

After that, we will give two other examples of minimal surfaces: **Enneper's surface** and **Scherk's surface**.

Given the minimal surface equation:

$$
f_{xx}(1 + f_y^2) - 2f_x f_y f_{xy} + f_{yy}(1 + f_x^2) = 0,
$$

where the function $f(x, y)$ has continuous second partial derivatives. Let $(r, \theta)$ be polar coordinates with $x = r \cos \theta$ and $y = r \sin \theta$, and define $h(r, \theta) = f(r \cos \theta, r \sin \theta)$. If $h(r, \theta) = h(r)$ is a function of $r$ only, we can attempt to reduce the minimal surface equation into an ordinary differential equation (ODE). By solving the ODE, we can obtain one particular solution.

#### Change of Variables

First, we need to compute $\theta_x$, $\theta_y$, $r_x$, $r_y$, $x_\theta$, $x_r$, $y_\theta$, and $y_r$. It is straightforward to find:

$$
\theta_x = -\frac{1}{r} \sin \theta, \quad \theta_y = \frac{1}{r} \cos \theta, \quad
r_x = \cos \theta, \quad r_y = \sin \theta,
$$

$$
x_r = \cos \theta, \quad y_r = \sin \theta, \quad
x_\theta = -r \sin \theta, \quad y_\theta = r \cos \theta.
$$

Next, calculate $h_r$ and $h_\theta$:

$$
h_r = f_x \cos \theta + f_y \sin \theta, \quad
h_\theta = -f_x r \sin \theta + f_y r \cos \theta.
$$

This forms a linear system of equations. Solving for $f_x$ and $f_y$:

$$
f_x = \cos \theta h_r - \frac{\sin \theta}{r} h_\theta, \quad
f_y = \sin \theta h_r + \frac{\cos \theta}{r} h_\theta.
$$

#### Reduction to ODE

By the chain rule, compute $f_{xx}$, $f_{yy}$, and $f_{xy}$:

$$
f_{xx} = h_{rr} \cos^2 \theta - \frac{2}{r} \sin \theta \cos \theta h_{r \theta} +
\frac{2}{r^2} \sin \theta \cos \theta h_\theta +
\frac{1}{r^2} \sin^2 \theta h_{\theta \theta} +
\frac{1}{r} \sin^2 \theta h_r,
$$

$$
f_{yy} = h_{rr} \sin^2 \theta + \frac{2}{r} \sin \theta \cos \theta h_{r \theta} -
\frac{2}{r^2} \sin \theta \cos \theta h_\theta +
\frac{1}{r^2} \cos^2 \theta h_{\theta \theta} +
\frac{1}{r} \cos^2 \theta h_r,
$$

$$
f_{xy} = \sin \theta \cos \theta h_{rr} +
\frac{\sin^2 \theta}{r^2} h_\theta - \frac{\sin^2 \theta}{r} h_{r \theta} -
\frac{\sin \theta \cos \theta}{r} h_r +
\frac{\cos^2 \theta}{r} h_{r \theta} - \frac{\cos^2 \theta}{r^2} h_{\theta \theta} -
\frac{\cos^2 \theta}{r^2} h_\theta.
$$

If $h(r, \theta)$ depends only on $r$, we simplify the minimal surface equation to:

$$
2r h_{rr} + h_r^3 + h_r = 0.
$$

#### Solution for the Catenoid

Solving the simplified ODE gives one particular solution, known as the **catenoid**:

$$
r = c \cosh \left(\frac{h - d}{c}\right),
$$

where $c$ and $d$ are constants.

#### Solution for the Helicoid

Similarly, if $h(r, \theta) = h(\theta)$, substituting into the minimal surface equation gives another particular solution, known as the **helicoid**:

$$
h = c \theta + d,
$$

where $c$ and $d$ are constants.