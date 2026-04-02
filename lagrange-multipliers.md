---
layout: default
title: Extrema with Constraint: Lagrang Multiplier
---

Tags: #Analysis #Examples 

> **Note**
> Here we are going to illustrate how to solve an optimization problem by Lagrange multiplier with some examples.

---
> **Example 1** 
> Find the maximum and minimum values of $f$ subject to the given constraint, if such values exist.
> 
> $$
> \begin{cases}
> & f(x,y) = x+y \\
> & x^2 + y^2 = 1
> \end{cases}
> $$

Let the Lagrangian be 

$$
\mathcal{L}(x,y) = f(x,y) + \lambda(x^2+y^2)
$$ 
then 

$$
\begin{aligned}  \partial_x \mathcal{L} & = 1 + 2 \lambda x \\ 
 \partial_y \mathcal{L} & = 1 + 2 \lambda y 
 \end{aligned} 
 $$ 
To each the extrema, we must have $\dfrac{\partial \mathcal{L}}{\partial x} = 0$ and $\dfrac{\partial \mathcal{L}}{\partial y} = 0$. Thus 
 $$
 x= y = -\frac{1}{2\lambda}$$ Substituting it into the constraint, we get $$x = y = \pm \frac{1}{\sqrt{2}} 
 $$ 
 
 Hence,
 
 $$
 f_{max} = \dfrac{2}{\sqrt{2}}, \quad f_{min} = -\dfrac{2}{\sqrt{2}}
 $$
 
 
>  **Example 2**
> Find the maximum and minimum values of $f$ subject to the given constraint, if such values exist.
> 
> $$
> \begin{aligned}
>  f(x,y) &= x^2+2y^2 \\
> x^2 + y^2  &\le 4
> \end{aligned}
> $$

The Lagrangian is  

$$\mathcal{L}(x,y) = x^2 + xy^2 + \lambda(x^2 + y^2)$$ 

then 

$$ \partial_x \mathcal{L} = x(2-2\lambda),\quad \partial_y \mathcal{L} = y(4-2\lambda) $$ 

If the partial derivatives of $\mathcal{L}$ are zero, then we have different possible combinations of $(x,y,\lambda)$: $$(0,\pm \, 2,2), \quad (\pm \, 2,0,1), \quad(0,0,\lambda \in \mathbb{R})$$
They correspond to different values of $f(x,y)$: $$f_1 = f_{max} = 8, \quad f_2 = 4,\quad f_3= f_{min}=0$$

> **Example 3**
> For each value of $\lambda$ the function $$f(x,y) = x^2 + y^2 - \lambda (2x+4y-15)$$ has a minimum value $m(\lambda)$.
>- (a) Find $m(\lambda)$.
>- (b) For which value of $\lambda$ is $m(\lambda)$ the largest and what is that maximum value ?
>- (c) Find the minimum value of $f(x,y) = x^2 + y^2$ subject to the constraint $2x+4y = 15$ using the method of Lagrange multiplier and evaluate $\lambda$.

To find $m(\lambda)$, we just need to compute the partial derivatives of $f(x,y)$: 

$$
\begin{split} & \partial_x f = 2x - 2\lambda \\ 
& \partial_y f = 2y - 4\lambda 
\end{split} 
$$

$\partial_x f = \partial_y f = 0$ implies that $x= \lambda$ and $y = 2\lambda$. If we substitute them into $f(x,y)$, we will obtain 
$$
m(\lambda) = \lambda^2 + 4\lambda^2 - \lambda(2\lambda + 8\lambda -15) = -5\lambda^2 - 15 \lambda
$$

The derivative of $m(\lambda)$ is 
$$
m'(\lambda) = -10\lambda-15
$$ 

and $\lambda = -\dfrac{3}{2} \implies m'(\lambda) = 0$. The maximum value is 

$$m(-\frac{3}{2}) = -\frac{45}{4} + \frac{45}{2} =\frac{45}{4}$$

In order to find the minimum value, the value of $\lambda$ is different from zero, and we have 
$$
\frac{x}{y}=\frac{\lambda}{2\lambda} = \frac{1}{2} \implies 2x = y
$$ 

Substituting this relation into the constraint, we get 

$$
2x + 4y = 10x = 15
$$ 

Therefore, we have $x = \dfrac{3}{2} = \lambda$ , $y=3$, and $f_{min} = \dfrac{45}{4}$ 

> **Example 4** 
> Suppose we are given the function
> $$
> f(x,y,z) = x^2 - y^2 + z^2
> $$ in the space $\mathbb{R}^3$ with coordinates $x, y, z$. We seek an extremum of this function on the plane $S$ defined by the equation
> $$
> F(x,y,z) = 2x-y-3 = 0.
> $$ 

Let us consider a Lagrangian such that $$\mathcal{L}(x,y,z) = f(x,y,z) - \lambda F(x,y,z)$$ Its partial derivatives are 

$$
\begin{cases} 
& \partial_x \mathcal{L} = 2x-2\lambda \\ & \partial_y \mathcal{L} = -2y + \lambda \\ 
& \partial_z\mathcal{L} = 2z  
\end{cases}
$$

The extremum will be reached as the partial derivatives are zero, meaning 

$$
x= \lambda, \quad y = \frac{\lambda}{2},\quad z = 0
$$

Substituting this into the constraint, we obtain $\lambda = 2$. Thus the function $f(x,y,z)$ has an extremum $$f_{max} = \lambda^2 - \frac{\lambda^2}{4} = 3$$ It is a local maximum because the quadratic form

$$
(\partial_{x_i}\partial_{x_j}\mathcal{L}(x_0)) \xi_i \,\xi_j
$$ 

is negative-definite.
 
 


