# UN/NU Comprehensive Math Compendium

Dense, reference-grade summary of mathematical foundations and applied formulas across major domains.

---

## 1. Algebra

**Identities**
\[
(a+b)^2=a^2+2ab+b^2,\quad (a-b)^2=a^2-2ab+b^2
\]
\[
(a+b)(a-b)=a^2-b^2
\]
\[
\sum_{k=1}^n k=\frac{n(n+1)}{2},\quad \sum_{k=1}^n k^2=\frac{n(n+1)(2n+1)}{6}
\]

**Binomial**
\[
(x+y)^n=\sum_{k=0}^n\binom{n}{k}x^{n-k}y^k
\]

**Polynomials**
- Factor theorem: \(f(a)=0 \Rightarrow (x-a)\) divides \(f(x)\)
- Roots of unity: \(x^n=1 \Rightarrow e^{i2\pi k/n}\)

---

## 2. Calculus

**Derivatives**
\[
(fg)'=f'g+fg',\quad (f/g)'=\frac{f'g-fg'}{g^2}
\]
\[
\frac{d}{dx}a^x=a^x\ln a,\quad \frac{d}{dx}\ln x=1/x
\]

**Integrals**
\[
\int x^n dx = \frac{x^{n+1}}{n+1}+C,\ n\ne -1
\]
\[
\int e^{ax}dx=\frac{e^{ax}}{a}+C
\]
\[
\int \frac{1}{1+x^2}dx=\tan^{-1}x+C
\]

**Multivariate**
\[
\nabla f=(\partial_x f, \partial_y f,\partial_z f)
\]
\[
\text{div}\,F=\nabla\cdot F,\quad \text{curl}\,F=\nabla\times F
\]

---

## 3. Linear Algebra

**Matrix operations**
\[
(A+B)^\top=A^\top+B^\top,\quad (AB)^\top=B^\top A^\top
\]
\[
(AB)^{-1}=B^{-1}A^{-1},\quad \det(AB)=\det A\,\det B
\]

**Norms**
\[
\|x\|_2=\sqrt{x^\top x},\quad \|A\|_F=\sqrt{\operatorname{tr}(A^\top A)}
\]

**Eigen and SVD**
\[
A x=\lambda x,\quad A=U\Sigma V^\top
\]

**Projection**
\[
P=A(A^\top A)^{-1}A^\top
\]

---

## 4. Probability

**Definitions**
\[
\mathbb{E}[X]=\sum_x xp(x),\quad \operatorname{Var}(X)=\mathbb{E}[X^2]-\mathbb{E}[X]^2
\]

**Key distributions**
| Distribution | PDF/PMF | Mean | Variance |
|---------------|----------|------|-----------|
| Bernoulli(p) | \(p^x(1-p)^{1-x}\) | p | p(1-p) |
| Normal(\(\mu,\sigma^2\)) | \(\frac{1}{\sqrt{2\pi\sigma^2}}e^{-(x-\mu)^2/(2\sigma^2)}\) | \(\mu\) | \(\sigma^2\) |
| Exponential(\(\lambda\)) | \(\lambda e^{-\lambda x}\) | \(1/\lambda\) | \(1/\lambda^2\) |

**Theorems**
- LLN: \(\bar X_n\to \mu\)
- CLT: \(\sqrt{n}(\bar X_n-\mu)\to \mathcal{N}(0,\sigma^2)\)
- Bayes: \(P(A|B)=\frac{P(B|A)P(A)}{P(B)}\)

---

## 5. Optimization

**Gradient methods**
\[
x_{k+1}=x_k-\eta \nabla f(x_k)
\]
**Newton**
\[
x_{k+1}=x_k-H^{-1}(x_k)\nabla f(x_k)
\]

**Constrained (Lagrange)**
\[
L(x,\lambda)=f(x)+\lambda^\top g(x)
\]
KKT conditions:
\[
\nabla_x L=0,\ g(x)\le0,\ \lambda\ge0,\ \lambda_i g_i(x)=0
\]

---

## 6. Discrete Math

**Counting**
\[
\binom{n}{k}=\frac{n!}{k!(n-k)!},\quad P(n,k)=\frac{n!}{(n-k)!}
\]
**Inclusion–exclusion**
\[
|A\cup B|=|A|+|B|-|A\cap B|
\]

**Graph basics**
\[
\sum_{v\in V}\deg(v)=2|E|
\]

---

## 7. Geometry and Trig

\[
\sin^2x+\cos^2x=1,\quad \tan x=\frac{\sin x}{\cos x}
\]
\[
\sin(a\pm b)=\sin a\cos b\pm\cos a\sin b
\]
Law of cosines:
\[
c^2=a^2+b^2-2ab\cos C
\]

---

## 8. Complex Analysis

\[
e^{i\theta}=\cos\theta+i\sin\theta
\]
Residue theorem:
\[
\oint_\gamma f(z)dz=2\pi i\sum \operatorname{Res}(f,z_k)
\]

---

## 9. Numerical Methods

**Root finding**
\[
x_{k+1}=x_k-\frac{f(x_k)}{f'(x_k)}
\]
**ODEs**
\[
x_{k+1}=x_k+h f(t_k,x_k)
\]

---

## 10. Machine Learning Core Math

**Linear regression**
\[
\hat\beta=(X^\top X)^{-1}X^\top y
\]
**Logistic**
\[
p(y|x)=\sigma(w^\top x)=\frac{1}{1+e^{-w^\top x}}
\]
**Loss**
\[
L=\frac{1}{n}\sum_i \log(1+e^{-y_i w^\top x_i})
\]
**Gradient**
\[
\nabla L=-\frac{1}{n}\sum_i \frac{y_i x_i}{1+e^{y_i w^\top x_i}}
\]

---

## 11. Information Theory

\[
H(X)=-\sum_x p(x)\log p(x)
\]
\[
D_{\mathrm{KL}}(p\|q)=\sum_x p(x)\log\frac{p(x)}{q(x)}
\]
\[
I(X;Y)=H(X)-H(X|Y)
\]

---

## 12. Special Functions

\[
\Gamma(z)=\int_0^\infty t^{z-1}e^{-t}dt,\quad B(x,y)=\int_0^1 t^{x-1}(1-t)^{y-1}dt
\]
\[
\operatorname{erf}(x)=\frac{2}{\sqrt{\pi}}\int_0^x e^{-t^2}dt
\]

---

File is intentionally condensed for UN/NU analytical use.

