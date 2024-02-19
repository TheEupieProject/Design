<<<<<<< HEAD
# Symbol list and testing

## Syntax

When writing a full document, a markdown-like syntax applies:

- Single line returns are ignored.

- 

## Some examples

> _Note: This is far from being finished (changes will occur), and far from being complete._
=======
> _Note: This is far from being finished (changes will occur), and far from being complete. Github LaTeX support is partial._
>>>>>>> 9a5df3c9eae97e0da99a0a4701055f61d10315ba

| Symbol                                                   | Eupie example                                                         | LaTeX version                                            |
| -------------------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------- |
| $50$                                                     | `50`                                                                  | `50`                                                     |
| $x$                                                      | `x`                                                                   | `x`                                                      |
| $\text{mass}$                                            | `mass`                                                                | `\text{mass}`                                            |
| $ab$                                                     | `a b`                                                                 | `ab`                                                     |
| $a+b$                                                    | `a+b`                                                                 | `a+b`                                                    |
| $a-b$                                                    | `a-b`                                                                 | `a-b`                                                    |
| $a \times b$                                             | `a * b`                                                               | `a \times b`                                             |
| $\frac{a}{b}$                                            | `a / b`                                                               | `\frac{a}{b}`                                            |
| $x^2$                                                    | `x^2`                                                                 | `x^2`                                                    |
| $x^{2ex}$                                                | `x^(2 e x)`                                                           | `x^{2ex}`                                                |
| $3 \times (5 + 4x)$                                      | `3 * (5 + 4x)`                                                        | `3 \times (5 + 4x)`                                      |
| $3 (5 + 4x)$                                             | `3(5 + 4x)`                                                           | `3(5 + 4x)`                                              |
| $5 + 3 \times x$                                         | `5+(3*x)`                                                             | `5+3\times x`                                            |
| $\vec{v}$                                                | given the previous declaration[^3]: <br> `v : vec`<br>simply:<br> `v` | `\vec{v}`                                                |
| $(3, 2)$                                                 | `(3, 2)`                                                              | `(3, 2)`                                                 |
| $(3\ ;2)$                                                | `(3 ;2)`[^1]                                                          | `(3\ ;2)`                                                |
| $\begin{pmatrix} x_{1} \\ x_{2} \end{pmatrix}$           | `vec(x_1, x_2)`[^2]                                                   | `\begin{bmatrix} x_{1} \\ x_{2} \end{bmatrix}`           |
| $\R$                                                     | `set(R)`                                                              | `\R`                                                     |
| $\mathbb{B}$                                             | `set(B)`                                                              | `\mathbb{B}`                                             |
| $2x = 1 \lrArr x = \frac{1}{2}$                          | `2x = 1 <=> x = 1/2`                                                  | `2x = 1 \lrArr x = \frac{1}{2}`                          |
| $-2x > 1 \rArr x < \frac{-1}{2}$                         | `-2x > 1 => x < -1/2`                                                 | `-2x > 1 \rArr x < \frac{-1}{2}`                         |
| $x \leq y$                                               | `x <= y`                                                              | `x \leq y`                                               |
| $x \geq y$                                               | `x >= y`                                                              | `x \geq y`                                               |
| $x \approx 3$                                            | `x ~= 3`                                                              | `x \approx 3`                                            |
| $\sqrt{\ln[\cos(x)]}$                                    | `sqrt(ln[cos(x)])`                                                    | `\sqrt{\ln[\cos(x)]}`                                    |
| $\lfloor \|x\| \rfloor$                                  | `floor(\|x\|)`                                                        | `\lfloor \|x\| \rfloor`                                  |
| $\sum_{i=0}^{+\infty} \prod_{j=1}^{+\infty} \frac{i}{j}$ | `sum(i=0, +inf) prod(j=1, +inf) i/j`                                  | `\sum_{i=0}^{+\infty} \prod_{j=1}^{+\infty} \frac{i}{j}` |
| $\forall x \in \R$                                       | `forall x in set(R)`                                                  | `\forall x \in \R`                                       |
| $\exist x \in \N_*$                                      | `exist x in set(N*)`                                                  | `\exist x \in \N_*`                                      |
| $\exist! n \in \N^+_*$                                   | `exist! x in set(N*+)`<mark>(`exist!` or `exist unique`?)</mark>      | `\exist! n \in \N^+_*`                                   |
| $x \ni y$                                                | `x suchthat y` <mark>(such that?)</mark>                              | `x \ni y`                                                |
| $k \in \Z$                                               | `k : set(Z)` (declaration)                                            | `k \in \Z`                                               |
| $Z \subset \Z$                                           | `Z : set`<br>`Z in set(Z)`[^4]                                        | `Z \subset \Z`                                           |
| $\mathbb{A} \cup \mathbb{B}$                             | `set(A) \|                                                            | set(B)`                                                  |
| $1\vee 0$                                                | `1 \|                                                                 | 0` (default behavior)                                    |
| $1 \wedge \neg 0 $                                       | `1 && !0`                                                             | `1 \wedge \neg 0`                                        |
| $\pi(\bar{E})$                                           | `pi(!E)` (default behavior for $\bar{E}$)                             | `\pi(\bar{E})`                                           |
| $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$           | `mat2x2(a, b, c, d)`[^5]                                              | `\begin{pmatrix} a & b \\ c & d \end{pmatrix}`           |
| $\alpha \beta \gamma \Gamma$                             | `alpha beta gamma Gamma`                                              | `\alpha \beta \gamma \Gamma`                             |
| $a \propto \aleph$                                       | `a =* aleph` (?)                                                      | `a \propto \aleph`                                       |
| $x \equiv y [\mod5] $                                    | `x <???> y[mod 5]` [TODO]                                             | `x \equiv y [\mod5]`                                     |

`forall x in set(R) suchthat 2|floor(x)`

`pourtout x dans ensemble(R) telque 2|seuil(x)` (translation ?)

`{2n \: forall n in set(N)}` (operator escaping ?)

$$
\begin{pmatrix} 1 & \dotsb & 1 \\ \vdots & \ddots \\ 1 & & 1 \end{pmatrix}
$$

```
mat3x3(
      1, ...,  1,
    ..., ...,   ,
      1,    ,  1
)
```

> _Note: I don't like it. It doesn't look good. It's not very readable._

$$
\begin{cases}
18x^2 + 3\exp(-x^2) = 3y \\
z\sin(z \times y) = z \times \cos(x) \\
z + 3 = 2
\end{cases} \\
\lrArr \begin{cases}
18x^2 + 3\exp(-x^2) = 3y \\
z\sin(z \times y) = z \times \cos(x) \\
z = -1
\end{cases} \\
$$

```
{ 18x^2 + 3exp(-x^2) = 3y
{ z sin(z * y) = z * cos(x)
{ z + 3 = 2
<=>
{ 18x^2 + 3exp(-x^2) = 3y
{ z sin(z * y) = z * cos(x)
{ z + 3 = 2
```



## Positioning tools

Using standard markdown LaTeX, there's no way to show the wanted result. The idea is, for example, with matrix multiplication, to be able to put one matrix on top of another, while keeping everything aligned. The ideal package for this job in LaTeX is `nicematrix`.

It would look something like that:

```
mat2x2(2, 0, 0, 2)
on_top(mat2x2(1, 2, 3, 4)) mat2x2(2, 4, 6, 8)
```





[^1]: Useless specified spaces will be understood as additional spaces (note that default LaTeX symbol spacing is accounted: '2 + 3' = '2+3', but '2   +  3' is different).

[^2]: You can specify in compilation target if you want: 
    1. Parenthesis vector: $\begin{pmatrix} a \\ b \end{pmatrix}$
    1. Brackets vector: $\begin{bmatrix} a \\ b \end{bmatrix}$
    1. Braces vector: $\begin{Bmatrix} a \\ b \end{Bmatrix}$
    1. Pipe "vector": $\begin{vmatrix} a \\ b \end{vmatrix}$

[^3]: Declaration aren't some abstract part of the language. You can actually declare very common stuff easily with Eupie's type awareness. These can be visible when rendered.

[^4]: This is a direct result of Eupie type awarness. However, you may want to explicitly state that $Z$ is a set and that $Z \in \Z$. This is possible, given $\mathsf{P}(\Z)$ (noted `P(set(Z))`, which is again an example of Eupie's type awareness). Simply write `Z in P(set(Z))` (which will keep $Z$'s type, but not write exactly what you wanted), or `Z : set(Z)` (which will change $Z$'s type).
