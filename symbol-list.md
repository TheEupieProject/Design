
> _Note: This is far from being finished (changes will occur), and far from being complete._

| Symbol | Eupie example | LaTeX version |
|-------------|---------------|---------------|
| $50$     | `50`            |  `50`            |
| $x$ | `x` | `x` |
| $\text{mass}$ | `mass` | `\text{mass}` |
| $ab$ | `a b` | `ab` |
| $a+b$ | `a+b` | `a+b` |
| $a-b$ | `a-b` | `a-b` |
| $a \times b$ | `a * b` | `a \times b` |
| $\frac{a}{b}$ | `a / b` | `\frac{a}{b}` |
| $x^2$ | `x^2` | `x^2` |
| $x^{2ex}$ | `x^(2 e x)` | `x^{2ex}` |
| $3 \times (5 + 4x)$ | `3 * (5 + 4x)` | `3 \times (5 + 4x)` |
| $3 (5 + 4x)$ | `3(5 + 4x)` | `3(5 + 4x)` |
| $5 + 3 \times x$ | `5+(3*x)` | `5+3\times x` |
| $\vec{v}$ | given the previous declaration[^3]: <br> `v : vec`<br>simply:<br> `v` | `\vec{v}` |
| $(3, 2)$ | `(3, 2)` | `(3, 2)` |
| $(3\ ;2)$ | `(3 ;2)`[^1] | `(3\ ;2)` |
| $\begin{pmatrix} x_{1} \\ x_{2} \end{pmatrix}$ | `vec(x_1, x_2)`[^2] | `\begin{bmatrix} x_{1} \\ x_{2} \end{bmatrix}` |
| $\R$ | `set(R)` | `\R` |
| $\mathbb{B}$ | `set(B)` | `\mathbb{B}` |
| $2x = 1 \lrArr x = \frac{1}{2}$ | `2x = 1 <=> x = 1/2` | `2x = 1 \lrArr x = \frac{1}{2}` |
| $-2x > 1 \rArr x < \frac{-1}{2}$ | `-2x > 1 => x < -1/2` | `-2x > 1 \rArr x < \frac{-1}{2}` |
| $x \leq y$ | `x <= y`| `x \leq y` |
| $x \geq y$ | `x >= y`| `x \geq y` |
| $x \approx 3$ | `x ~= 3` | `x \approx 3` |
| $\sqrt{\ln[\cos(x)]}$ | `sqrt(ln[cos(x)])` | `\sqrt{\ln[\cos(x)]}` |
| $\lfloor \|x\| \rfloor$ | `floor(\|x\|)` | `\lfloor \|x\| \rfloor` |
| $\sum_{i=0}^{+\infty} \prod_{j=1}^{+\infty} \frac{i}{j}$ | `sum(i=0, +inf) prod(j=1, +inf) i/j` | `\sum_{i=0}^{+\infty} \prod_{j=1}^{+\infty} \frac{i}{j}` |
| $\forall x \in \R$ | `for x in set(R)`<mark>(for?)</mark> | `\forall x \in \R` |
| $\exist x \in \N_*$ | `exist x in set(N*)` | `\exist x \in \N_*` |
| $\exist! n \in \N^+_*$ | `exist! x in set(N*+)`<mark>(`exist!` or `exist unique`?)</mark> | `\exist! n \in \N^+_*` |
| $x \ni y$ | `x such that y` <mark>(such that?)</mark> | `x \ni y` |
| $k \in \Z$ | `k : set(Z)` (declaration) | `k \in \Z` |
| $Z \subset \Z$ | `Z : set`<br>`Z in set(Z)`[^4] | `Z \subset \Z` |

`for x in set(R) such that 2|floor(x)`

`pour x dans ensemble(R) tel que 2|seuil(x)` (translation ?)

`{2n \: for n in set(N)}` (operator escaping ?)

[^1]: Useless specified spaces will be understood as additional spaces (note that default LaTeX symbol spacing is accounted: '2 + 3' = '2+3', but '2   +  3' is different).

[^2]: You can specify in compilation target if you want: 
	1. Parenthesis vector: $\begin{pmatrix} a \\ b \end{pmatrix}$
	1. Brackets vector: $\begin{bmatrix} a \\ b \end{bmatrix}$
	1. Braces vector: $\begin{Bmatrix} a \\ b \end{Bmatrix}$
	1. Pipe "vector": $\begin{vmatrix} a \\ b \end{vmatrix}$

[^3]: Declaration aren't some abstract part of the language. You can actually declare very common stuff easily with Eupie's type awareness. These can be visible when rendered.

[^4]: This is a direct result of Eupie type awarness. However, you may want to explicitly state that $Z$ is a set and that $Z \in \Z$. This is possible, given $\mathsf{P}(\Z)$ (noted `P(set(Z))`, which is again an example of Eupie's type awareness). Simply write `Z in P(set(Z))` (which will keep $Z$'s type, but not write exactly what you wanted), or `Z : set(Z)` (which will change $Z$'s type).
