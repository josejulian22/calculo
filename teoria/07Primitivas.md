---
title: "Tema 7 - Cálculo de Primitivas"
author: "Juan Gabriel Gomila, Arnau Mir y Llorenç Valverde"
date: ''
output: 
  ioslides_presentation:
    widescreen: true
    css: Mery_style.css
    logo: Images/calculus.gif
    fig_caption: yes
    keep_md: yes
---
<script src="https://kit.fontawesome.com/a0edb659c7.js" crossorigin="anonymous"></script>




# Introducción

## Introducción al cálculo de primitivas
En el tema anterior, vimos que para calcular la **integral definida** de una función $f$ integrable en un cierto intervalo $[a,b]$, es fundamental saber calcular una **primitiva** $F$ de dicha función ya que dicha integral, usando la **regla de Barrow**, se puede escribir de la siguiente forma:
$$
\int_a^b f(x)\, dx = F(b)-F(a).
$$

En este tema, vamos a dar las técnicas para calcular **primitivas** de las funciones más usuales como pueden ser funciones **polinómicas**, **racionales**, **trigonométricas**, funciones definidas como la raíz cuadrada de un polinomio hasta de grado 2, etc.

## Introducción al cálculo de primitivas
Recordad que dada una función $f:[a,b]\longrightarrow\mathbb{R}$ definida en un intervalo $[a,b]$, una **primitiva** es una función $F:[a,b]\longrightarrow\mathbb{R}$ definida en el mismo intervalo tal que $F'(x)=f(x)$. 

Ésta es la razón que la **primitiva** de una función también se llame **antiderivada** ya que hallar **primitivas** es la operación **inversa** respecto a la operación de **derivar**. Si **derivar** es equivalente a dar un paso hacia delante, hallar una **primitiva** es dar un paso hacia atrás.

Recordemos que, dada una función $f$, existen una multitud de **primitivas** de la misma: dada una **primitiva** $F(x)$ de la misma, la función $F(x)+C$ donde $C$ es una constante cualquiera es también otra primitiva ya que si $F'(x)=f(x)$, también se cumple que $(F(x)+C)'=f(x)$.

## Introducción al cálculo de primitivas
A hallar una **primitiva** de una función $f$ también se conoce como hallar una **integral indefinida** de dicha función y lo denotaremos por:
$$
\int f(x)\, dx = F(x)+C,
$$
sin escribir los extremos de integración y añadiendo una constante cualquiera $C$ para poder de manifiesto que, como hemos indicado antes, existen una multitud de primitivas.

## Introducción al cálculo de primitivas
Supongamos que para una función $f$ particular, nos dan una **primitiva** $F$. Es decir $F'(x)=f(x)$ o $\displaystyle\int f(x)\, dx=F(x)+C$. 

Entonces, si en lugar de considerar la función $f$ consideramos la función siguiente $f(g(x))\cdot g'(x)$, donde $g(x)$ es una función cualquiera, tenemos que una **primitiva** de dicha función es $(F\circ g)(x)=F(g(x))$ ya que usando la regla de la cadena 
$$
(F\circ g)'(x)=F'(g(x))\cdot g'(x)=f(g(x))\cdot g'(x),
$$
como queríamos ver.

## Introducción al cálculo de primitivas
Es decir, si $\displaystyle\int f(x)\,dx =F(x)+C$, entonces $\displaystyle\int f(g(x))\cdot g'(x)\,dx = F(g(x))+C$.

En resumen, si somos capaces de hallar una **primitiva** para una cierta función $f$, somos capaces de hallar una **primitiva** para toda la familia de funciones $f(g(x))\cdot g'(x)$, donde $g(x)$ es una función cualquiera.

Hagamos un ejemplo ilustrativo.

## Introducción al cálculo de primitivas
<div class="example">
**Ejemplo**

En el capítulo anterior, vimos que una primitiva de la función monomio $f(x)=x^n$, con $n\geq 1$ natural era $F(x)=\frac{x^{n+1}}{n+1}+C$:
$$
\int x^n\, dx = \frac{x^{n+1}}{n+1}+C.
$$

La comprobación es muy fácil.

Usando lo que hemos dicho anteriormente, tenemos que una primitiva de la función $g(x)^n\cdot g'(x)$, donde $g$ es una función cualquiera, es $\frac{g(x)^{n+1}}{n+1}+C$:
$$
\int g(x)^n\cdot g'(x)\, dx = \frac{g(x)^{n+1}}{n+1}+C.
$$
</div>

## Introducción al cálculo de primitivas
<div class="example">
Por ejemplo, si consideramos $g(x)=\sin x$, podemos escribir: $\displaystyle \int \sin^n x\cdot \cos x\, dx =\frac{\sin^{n+1}x}{n+1}+C$.

Si consideramos $g(x)=4x^2+2$, podemos escribir: $\displaystyle \int (4x+2)^n \cdot 4\, dx =\frac{(4x+2)^{n+1}}{n+1}+C$.

Si consideramos $g(x)=\ln x$, podemos escribir: $\displaystyle \int \frac{(\ln x)^n}{x} \, dx =\frac{(\ln x)^{n+1}}{n+1}+C$.

Y así sucesivamente, eligiendo la función $g$ que queramos.
</div>

En resumen, cualquier fórmula de cálculo de **primitivas** de una cierta función $f$, equivale a tener un conjunto de fórmulas de cálculo de **primitivas** de la familia de funciones $f(g(x))\cdot g'(x)$, para cualquier función $g$.

## Introducción al cálculo de primitivas
Hemos de pensar que para la mayoría de las funciones no se puede hallar una **primitiva** usando las técnicas explicadas en este capítulo. 

Es decir, dada una función $f:[a,b]\longrightarrow\mathbb{R}$ **integrable**, una función **primitiva** sería 
$$
F(x)=\int_a^x f(t)\, dt.
$$
El problema es que, en general, no podemos hallar una expresión de $F(x)$ en términos de funciones conocidas.
Se tienen que usar técnicas de **análisis numérico** para hallar la integral definida correspondiente.

# Integrales inmediatas

## Integrales inmediatas
Vamos a dar una lista de **integrales indefinidas** que serán la base para el cálculo de las demás. 

Les llamaremos **integrales inmediatas** ya que para ver su veracidad, basta derivar la expresión correspondiente y ver que el resultado de la derivada es la función que integramos.

En cada fila, vamos a considerar aparte de la **integral inmediata** correspondiente, la versión de dicha integral usando una función cualquiera $g(x)$ tal como hemos comentado en la introducción.

## Integrales inmediatas
<div class="center">
|| || 
|:---:|:---:|
|$\displaystyle\int x^n\, dx = \frac{x^{n+1}}{n+1}+C,\ n\neq -1$ | $\displaystyle\int g(x)^n\cdot g'(x)\, dx = \frac{g(x)^{n+1}}{n+1}+C,\ n\neq -1$
|$\displaystyle\int \frac{1}{x}\, dx =\ln |x|+C$|$\displaystyle\int \frac{g'(x)}{g(x)}\, dx =\ln |g(x)|+C$|
|$\displaystyle \int a^x dx = {a^x \over \ln a} + C, \; a> 0,\; a\not = 1$|$\displaystyle \int a^{g(x)}\cdot g'(x) dx = {a^{g(x)} \over \ln a} + C, \; a> 0,\; a\not = 1$|
|$\displaystyle \int e^x dx = e^x + C$|$\displaystyle \int e^{g(x)}\cdot g'(x) dx = e^{g(x)} + C$|
|$\displaystyle \int \sin x dx = -\cos x +C$|$\displaystyle \int \sin (g(x))\cdot g'(x) dx = -\cos (g(x)) +C$|
</div>

## Integrales inmediatas
<div class="center">
|| || 
|:---:|:---:|
|$\displaystyle \int \cos x dx = \sin x + C$|$\displaystyle \int \cos (g(x))\cdot g'(x) dx = \sin (g(x)) + C$|
|$\displaystyle \int {dx \over \cos^2 x } = \tan x + C$|$\displaystyle \int {g'(x) dx \over \cos^2 (g(x)) } = \tan (g(x)) + C$|
|$\displaystyle \int {dx \over\sin^2 x } = -\cot x + C$|$\displaystyle \int {g'(x)dx \over\sin^2 (g(x)) } = -\cot (g(x)) + C$|
|$\displaystyle \int {dx \over 1+x^2} = \arctan x + C$|$\displaystyle \int {g'(x)dx \over 1+g(x)^2} = \arctan (g(x)) + C$|
|$\displaystyle \int {dx \over \sqrt{1-x^2} }= \arcsin x + C$|$\displaystyle \int {g'(x)dx \over \sqrt{1-g(x)^2} }= \arcsin (g(x)) + C$|
</div>

# Integración de funciones racionales

## Introducción
En esta sección vamos a aprender técnicas para calcular **integrales indefinidas** de funciones racionales, es decir, funciones del tipo $\frac{P(x)}{Q(x)}$ donde $P(x)$ y $Q(x)$ son polinomios a coeficientes reales.

Distinguiremos dos casos:

**Primer caso:** Supongamos que el grado del polinomio $P(x)$ es mayor o igual que el grado del polinomio $Q(x)$: $\mathrm{grado}(P)\geq \mathrm{grado}(Q)$.

En este caso, hemos de dividir el polinomio $P(x)$ entre el polinomio $Q(x)$ obteniendo un cociente $C(x)$ y un resto $R(x)$, donde $\mathrm{grado}(R) < \mathrm{grado}(Q)$. 

## Caso en que el grado del numerador es mayor o igual que el del denominador
La relación entre los cuatro polinomios anteriores es la siguiente:
$$
P(x)=Q(x)\cdot C(x)+R(x).
$$
Si dividimos la expresión anterior por el polinomio $Q(x)$, obtenemos:
$$
\frac{P(x)}{Q(x)}=C(x)+\frac{R(x)}{Q(x)},
$$
y podemos escribir la integral indefinida de la función racional $\frac{P(x)}{Q(x)}$ como:
$$
\int \frac{P(x)}{Q(x)}\, dx=\int C(x)\, dx+\int \frac{R(x)}{Q(x)}\, dx.
$$

## Caso en que el grado del numerador es mayor o igual que el del denominador
La integral indefinida $\displaystyle\int C(x)\, dx$ es sencilla de calcular ya que se trata de la integral indefinida de un polinomio que se puede escribir como la suma de integrales de monomios de la forma $\displaystyle\int x^k\, dx$ multiplicadas por constantes. Las integrales $\displaystyle \int x^k\, dx$ valen $\frac{x^{k+1}}{k+1}+C$ como está indicado en la tabla de integrales inmediatas.


## Caso en que el grado del numerador es mayor o igual que el del denominador
La integral restante $\displaystyle \int \frac{R(x)}{Q(x)}\, dx$ se trata de una integral racional con la particularidad de que el grado del denominador es menor que el grado del numerado que sería el segundo caso a considerar.

En resumen, dada una integral racional, siempre podemos suponer que el grado del denominador es menor estricto que el grado del numerador ya que, en caso contrario, realizaríamos la operación indicada y estaríamos en este caso.



## Caso en que el grado del numerador es menor que el del denominador

**Segundo caso:** Supongamos que el grado del polinomio $P(x)$ es menor estrictamente que el grado del polinomio $Q(x)$: $\mathrm{grado}(P)< \mathrm{grado}(Q)$.

Supondremos además que el polinomio $Q(x)$ del denominador es mónico, es decir, el coeficiente correspondiente al término principal o del monomio de mayor grado vale 1. Si éste no fuera el caso, dividimos todos los términos por dicho coeficiente y "sacamos" fuera de la integral dicho coeficiente. 

## Caso en que el grado del numerador es menor que el del denominador
Más concretamente, supongamos que $Q(x)=C x^q+\cdots$, donde $q$ es el grado del denominador $Q(x)$. En este caso hacemos lo siguiente:
$$
\int \frac{P(x)}{Q(x)}\, dx =\frac{1}{C}\int \frac{P(x)}{\frac{Q(x)}{C}}\, dx,
$$
y ahora el polinomio $\frac{Q(x)}{C}$ sería mónico. Por tanto, si no lo fuera, realizamos la operación indicada anteriormente y ya estaríamos en el caso en que el denominador es mónico.

## Caso en que el grado del numerador es menor que el del denominador
Seguidamente, descomponemos el denominador $Q(x)$ de la siguiente manera:
$$
\begin{array}{rl}
Q(x)= & (x-a_1)^{n_1}\cdot (x-a_2)^{n_2}\cdots (x-a_k)^{n_k}\cdot \\ & ((x-b_1)^2+c_1^2)^{m_1}\cdot ((x-b_2)^2+c_2^2)^{m_2}\cdots ((x-b_l)^2+c_l^2)^{m_l},
\end{array}
$$
donde $a_1, \ldots, a_k$ serían las raíces reales de multiplicidad $n_1,\ldots, n_k$, respectivamente y los términos $((x-b_1)^2+c_1^2),\ldots,((x-b_l)^2+c_l^2)$ representan los términos de las raíces no reales de multiplicidad $m_1\ldots,m_l$, respectivamente.

## Descomposición de la fracción racional
<div class="exercise">
**Ejercicio**

Sea $P(x)$ un polinomio de grado $n$ con coeficientes reales, es decir,
$$
P(x)=\alpha_0 +\alpha_1 x+\cdots + \alpha_n x^n,
$$
con $\alpha_i\in\mathbb{R}$, $i=0,1,\ldots,n$.

Demostrar que si $z=z_1 +\mathrm{i} z_2$, $z_1,\ z_2\in\mathbb{R}$, es una raíz compleja del polinomio $P(x)$, es decir $P(z)=0$, también lo es su conjugada $\overline{z}=z_1-\mathrm{i}z_2$, $P(\overline{z})=0$, y en este caso, el polinomio $P(x)$ es divisible por el polinomio de segundo grado $(x^2-2 z_1 x+z_1^2 +z_2^2)$.

Los números complejos están introducidos en el curso de Álgebra lineal:

https://www.udemy.com/course/algebralineal/?couponCode=51CABC7FFF4982E6CBB7

</div>

## Descomposición de la fracción racional
En primer lugar, supongamos que estamos en el caso en que las multiplicidades de los términos correspondientes a las raíces no reales son simples, es decir, suponemos que $m_1=\cdots =m_l=1$.

A continuación, descomponemos la fracción racional $\frac{P(x)}{Q(x)}$ de la siguiente manera:
$$
\begin{array}{rl}
\frac{P(x)}{Q(x)} = & \frac{A_{11}}{x-a_1}+\frac{A_{12}}{(x-a_1)^2}+\cdots +\frac{A_{1n_1}}{(x-a_1)^{n_1}}+\cdots \\ 
& +\frac{A_{k1}}{x-a_k}+\frac{A_{k2}}{(x-a_k)^2}+\cdots +\frac{A_{kn_k}}{(x-a_k)^{n_k}}\\ & +\frac{B_1x+C_1}{((x-b_1)^2+c_1^2)}+\cdots + \frac{B_l x+C_l}{((x-b_l)^2+c_l^2)}
\end{array}
$$
hallando los coeficientes $A_{ij}$, $B_i$ y $C_i$ correspondientes.

## Descomposición de la fracción racional
Para hallar dichos coeficientes hemos de sumar la parte de la derecha de la igualdad anterior reduciendo a común denominador y nos quedará una igualdad del tipo:
$$
\frac{P(x)}{Q(x)}=\frac{H(x)}{Q(x)},
$$
donde los coeficientes del polinomio $H(x)$ dependen de los coeficientes $A_{ij}$, $B_i$ y $C_i$. 
A continuación, para $k=1,\ldots, \mathrm{grado\ } P$, igualamos los coeficientes de $x^k$ del polinomio $P(x)$ y del polinomio $H(x)$. 

Al final nos saldrá un sistema de ecuaciones lineal en los coeficientes $A_{ij}$, $B_i$ y $C_i$ que tendremos que resolver.

## Descomposición de la integral indefinida
Una vez hallados los coeficientes $A_{ij}$, $B_i$ y $C_i$, descomponemos la integral racional $\displaystyle\int\frac{P(x)}{Q(x)}\, dx$ de la siguiente manera:
$$
\begin{array}{rl}
\displaystyle\int\frac{P(x)}{Q(x)}\, dx = & \displaystyle A_{11}\int\frac{1}{x-a_1}\, dx+\cdots +A_{1n_1}\int \frac{1}{(x-a_1)^{n_1}}\, dx + \\ & \displaystyle +\cdots +A_{k1}\int \frac{1}{x-a_k}\, dx +\cdots +A_{kn_k}\int \frac{1}{(x-a_k)^{n_k}}\, dx+\\ & \displaystyle + \int \frac{B_1x+C_1}{((x-b_1)^2+c_1^2)}\, dx+\cdots + \int\frac{B_l x+C_l}{((x-b_l)^2+c_l^2)}\, dx.
\end{array}
$$

## Cálculo de las integrales indefinidas de la descomposición
Hemos reducido el problema a hallar integrales indefinidas del tipo:
$$
\int \frac{1}{(x-a)^i}\, dx,\quad \int\frac{Bx+D}{(x-b)^2+c^2}\, dx,
$$
para $i=1,2,\ldots$

## Cálculo de las integrales indefinidas de la descomposición
El valor de las integrales indefinidas del tipo $\displaystyle\int \frac{1}{(x-a)^i}\, dx$ es el siguiente:

* si $i=1$: $\displaystyle\int \frac{1}{(x-a)}\, dx=\ln |x-a|+C$, ver la segunda fila de la tabla de integrales inmediatas con $g(x)=x-a$.

## Cálculo de las integrales indefinidas de la descomposición
* si $i\geq 2$: 
$$
\begin{array}{rl}
\displaystyle\int \frac{1}{(x-a)^i}\, dx & =  \displaystyle \int (x-a)^{-i}\, dx =\frac{(x-a)^{-i+1}}{-i+1}+C \\ & \displaystyle =\frac{1}{(1-i)\cdot (x-a)^{i-1}}+C,
\end{array}
$$ 
ver la primera fila de la tabla de integrales inmediatas con $g(x)=x-a$.

## Cálculo de las integrales indefinidas de la descomposición
El cálculo de las integrales del tipo $\displaystyle \int\frac{Bx+D}{(x-b)^2+c^2}\, dx$ es el siguiente:
$$
\begin{array}{rl}
\displaystyle\int\frac{Bx+D}{(x-b)^2+c^2}\, dx & \displaystyle =\frac{B}{2}\int \frac{2x+\frac{2D}{B}}{(x-b)^2+c^2}\, dx\\  & =\displaystyle \frac{B}{2}\int \frac{2(x-b)+2b+\frac{2D}{B}}{(x-b)^2+c^2}\, dx \\ & \displaystyle = \frac{B}{2}\int \frac{2(x-b)}{(x-b)^2+c^2}\, dx +\frac{B}{2}\int \frac{2b+\frac{2D}{B}}{(x-b)^2+c^2}\, dx
\end{array}
$$

## Cálculo de las integrales indefinidas de la descomposición
La primera de la integrales anteriores $\displaystyle \frac{B}{2}\int \frac{2(x-b)}{(x-b)^2+c^2}\, dx$ es inmediata, ver segunda fila de la tabla de integrales inmediatas, con $g(x)=(x-b)^2+c^2$:
$$
\frac{B}{2}\int \frac{2(x-b)}{(x-b)^2+c^2}\, dx =\frac{B}{2}\ln |(x-b)^2+c^2|+C
$$

## Cálculo de las integrales indefinidas de la descomposición
El cálculo de la segunda integral es el siguiente:
$$
\begin{array}{rl}
\displaystyle\frac{B}{2}\int \frac{2b+\frac{2D}{B}}{(x-b)^2+c^2}\, dx  & \displaystyle =B\left(b+\frac{D}{B}\right)\int  \frac{1}{(x-b)^2+c^2}\, dx\\ & \displaystyle =\frac{B b+D}{c^2}\int \frac{1}{\left(\frac{x-b}{c}\right)^2+1}\, dx\\ & \displaystyle =\frac{B b+D}{c} \int \frac{\frac{1}{c}}{\left(\frac{x-b}{c}\right)^2+1}\, dx
\end{array}
$$

## Cálculo de las integrales indefinidas de la descomposición
La integral $\displaystyle \int \frac{\frac{1}{c}}{\left(\frac{x-b}{c}\right)^2+1}\, dx$ es inmediata, ver novena fila de la tabla de integrales inmediatas con $g(x)=\frac{x-b}{c}$:
$$
\int \frac{\frac{1}{c}}{\left(\frac{x-b}{c}\right)^2+1}\, dx =\arctan\left(\frac{x-b}{c}\right)+C.
$$

## Cálculo de las integrales indefinidas de la descomposición
En resumen:
$$
\int\frac{Bx+D}{(x-b)^2+c^2}\, dx = \frac{B}{2}\ln |(x-b)^2+c^2|+\frac{(B b+D)}{c}\arctan\left(\frac{x-b}{c}\right)+C.
$$

## Método de Ostrogradski
Falta estudiar el caso en que algún $m_i >1$, donde $i$ puede ser $i=1,\ldots,l$. 

En este caso, aplicaremos el llamado **Método de Ostrogradski**. 

Recordemos que tenemos que hallar la integral indefinida $\displaystyle \int\frac{P(x)}{Q(x)}\, dx$ donde suponemos que $\mathrm{grado\ }P<\mathrm{\ grado\ }Q$.

## Método de Ostrogradski
Dicho método consiste en descomponer la integral indefinida a calcular de la siguiente manera:
$$
\int\frac{P(x)}{Q(x)}\, dx = \frac{R(x)}{Q_1(x)}+\int\frac{T(x)}{Q_2(x)}\, dx,
$$
donde $Q_1(x)=\mathrm{mcd}(Q(x),Q'(x))$, es decir, el máximo común divisor entre los polinomios $Q(x)$ y su derivada $Q'(x)$ y $Q_2 =\frac{Q(x)}{Q_1(x)}$ es el cociente que resulta de dividir el polinomio $Q(x)$ por el polinomio $Q_1(x)$.

## Método de Ostrogradski
Los polinomios $R(x)$ y $T(x)$ son polinomios de grados $\mathrm{grado\ }Q_1-1$ y $\mathrm{grado\ }Q_2-1$, respectivamente cuyos coeficientes se tienen que hallar derivando la descomposición anterior:
$$
\frac{P(x)}{Q(x)} =\frac{R'(x)\cdot Q_1(x)-R(x)\cdot Q_1'(x)}{Q_1(x)^2}+\frac{T(x)}{Q_2(x)}.
$$

Si volvemos a aplicar el método propuesto al cálculo de la integral racional $\displaystyle\int\frac{T(x)}{Q_2(x)}\, dx$, los posibles exponentes $m_i$ serán como máximo todos $1$ que es el caso que se ha analizado.

# Integrales trigonométricas

## Introducción
En esta sección vamos a aprender a calcular integrales indefinidas que involucren funciones trigonométricas básicas como $\sin x$, $\cos x$ y $\tan x$:

* $\displaystyle \int \sin^m x\cos^n x\, dx$, donde $m$ y $n$ son números naturales.
* $\displaystyle \int \tan^n x\, dx,\ \int \cot^n x$ donde $n$ es un número natural.
* $\displaystyle \int \sin (m x)\cos (n x)\, dx$, donde $m$ y $n$ son números naturales.
* $\displaystyle \int R(\sin x, \cos x)\, dx$ donde $R(\sin x,\cos x)$ quiere decir una función racional en las variables $\sin x$ y $\cos x$ como por ejemplo $R(\sin x,\cos x)=\frac{\sin^2 x +\cos x+1}{\cos^2 x-\cos x-1}$.

## Introducción
Recordemos las identidades trigonométricas que usaremos en el cálculo de las integrales anteriores:

* Seno de la suma/diferencia:
$$
\sin (A\pm B)=\sin A\cdot cos B\pm \cos A\cdot \sin B.
$$

* El seno del ángulo doble: 

$$\sin (2x)=2\sin x\cos x.$$

## Introducción
* Coseno de la suma/diferencia:
$$
\cos (A\pm B)=\cos A\cdot \cos B\mp \sin A\cdot \sin B.
$$

* El coseno del ángulo doble: 

$$\cos (2x)=\cos^2 x-\sin^2 x=2\cos^2 x-1=1-2\sin^2 x.$$ 

## Introducción

* De las identidades anteriores tenemos que 

$$\sin^2 x=\frac{1}{2}(1-\cos (2x)),\ \cos^2 x=\frac{1}{2}(1+\cos (2x)).$$

* Relación entre el coseno y la tangente: 

$$1+\tan^2 x=\frac{1}{\cos^2 x},$$ 

o, si se quiere $$\tan^2 x=\sec^2 x-1 \ \mathrm{o}, \ \cot^2 x=\csc^2x -1.$$

## Introducción

* Fórmulas que transforman productos en sumas:
$$
\begin{array}{rl}
\sin x\cos y & = \frac{1}{2}(\sin (x+y)+\sin (x-y)),\\
\cos x\cos y & = \frac{1}{2}(\cos (x+y)+\cos (x-y)),\\
\sin x\sin y & = \frac{1}{2}(\cos (x-y)-\cos (x+y)).
\end{array}
$$
Las expresiones anteriores se pueden generalizar:
$$
\begin{array}{rl}
\sin(m x)\cos (ny) & = \frac{1}{2}(\sin (mx+ny)+\sin (mx-ny)),\\
\cos(m x)\cos (ny) & = \frac{1}{2}(\cos (mx+ny)+\cos (mx-ny)),\\
\sin(m x)\sin (ny) & = \frac{1}{2}(\cos (mx-ny)-\cos (mx+ny)),
\end{array}
$$
donde $m$ y $n$ son números naturales.


## Integrales indefinidas de $\sin^m x\cos^n x$
En esta sección vamos a explicar cómo calcular el siguiente tipo de integrales inmediatas $\displaystyle\int \sin^m x\cos^n x\, dx$, con $n$ y $m$ números naturales.

Vamos a distinguir los casos siguientes:

* 1: Uno de los números $n$ o $m$ es cero. En este caso, distinguimos los subcasos siguientes:

## Integrales indefinidas de $\sin^m x\cos^n x$

**1.1: $m$ impar**. En este caso, existe un natural $m_1$ tal que $m=2m_1+1$. La integral indefinida a calcular sería:
$$
\int\sin^{2m_1+1}x\, dx =\int (\sin^2 x)^{m_1}\sin x\, dx=\int (1-\cos^2 x)^{m_1}\sin x\, dx.
$$

A continuación, si desarrollamos la expresión $(1-\cos^2 x)^{m_1}$ nos quedará una suma de integrales de la forma $\displaystyle\int \cos^j x\sin x\, dx$, con $j$ natural. Dichas integrales son inmediatas y corresponden a la primera fila de la tabla de integrales inmediatas con $g(x)=\cos x$:
$$
\int \cos^j x\sin x\, dx =-\int \cos^j x (-\sin x)\, dx = -\frac{\cos^{j+1}x}{(j+1)}+C.
$$

## Integrales indefinidas de $\sin^m x\cos^n x$

**1.2: $n$ impar**. En este caso, existe un natural $n_1$ tal que $n=2n_1+1$. Este caso es parecido al anterior:
$$
\int\cos^{2n_1+1}x\, dx =\int (\cos^2 x)^{n_1}\cos x\, dx=\int (1-\sin^2 x)^{n_1}\cos x\, dx.
$$

A continuación, si desarrollamos la expresión $(1-\sin^2 x)^{n_1}$ nos quedará una suma de integrales de la forma $\displaystyle\int \sin^j x\cos x\, dx$, con $j$ natural. Dichas integrales son inmediatas y corresponden a la primera fila de la tabla de integrales inmediatas con $g(x)=\sin x$:

$$
\int \sin^j x\cos x\, dx =\frac{\sin^{j+1}x}{(j+1)}+C.
$$


## Integrales indefinidas de $\sin^m x\cos^n x$
**1.3 $n$ par**. En este caso, existe un natural $n_1$ tal que $n=2n_1$. El cálculo de la integral es el siguiente:

$$
\begin{array}{rl}
\displaystyle\int \cos^{2n_1} x\, dx & =\displaystyle \int (\cos^2 x)^{n_1}\, dx  = \int\left(\frac{1+\cos(2x)}{2}\right)^{n_1}\, dx
\\ & = \displaystyle \frac{1}{2^{n_1+1}}\int (1+\cos t)^{n_1}\, dt,
\end{array}
$$
donde en la última igualdad hemos hecho el cambio de variable $t=2x$. 

## Integrales indefinidas de $\sin^m x\cos^n x$
Seguidamente si desarrollamos $(1+\cos t)^{n_1}$ nos van saliento integrales del tipo $\displaystyle \int \cos^j x\, dx$ donde si $j$ es impar, ya las hemos estudiado en el apartado 1.2 y si $j$ es par, hemos reducido el exponente a la mitad. En el peor de los casos nos saldría la integral $\displaystyle\int\cos^2 x\,dx$ que se resolvería de la forma siguiente:
$$
\begin{array}{rl}
\displaystyle \int\cos^2 x\, dx & \displaystyle  = \frac{1}{2}\int (1+\cos (2x))\, dx = \frac{1}{2}\left(x+\frac{\sin(2x)}{2}\right)+C \\ & \displaystyle  =\frac{1}{2}x+\frac{1}{4}\sin (2x)+C
\end{array}
$$

## Integrales indefinidas de $\sin^m x\cos^n x$

**1.4 $m$ par**. En este caso, existe un natural $m_1$ tal que $m=2m_1$. El cálculo de la integral es el siguiente:
$$
\begin{array}{rl}
\displaystyle\int \sin^{2m_1} x\, dx & =\displaystyle \int (\sin^2 x)^{m_1}\, dx  = \int\left(\frac{1-\cos(2x)}{2}\right)^{m_1}\, dx
\\ & = \displaystyle \frac{1}{2^{m_1+1}}\int (1-\cos t)^{m_1}\, dt,
\end{array}
$$
donde en la última igualdad hemos hecho el cambio de variable $t=2x$.  Seguidamente si desarrollamos $(1+\cos t)^{m_1}$ nos van saliento integrales del tipo $\displaystyle \int \cos^j x\, dx$ que ya están estudiadas en los apartados 1.2 y 1.3.

## Integrales indefinidas de $\sin^m x\cos^n x$
* 2: Uno de los números $n$ o $m$ es par y el otro, $impar$. 

**2.1: $m$ es impar y $n$ es par**. En este caso, existen dos naturales más, $m_1$ y $n_1$ tal que $m=2m_1+1$ y $n=2n_1$. Para resolver la integral inmediata, hacemos lo siguiente:
$$
\begin{array}{rl}
\displaystyle\int \sin^{2m_1+1}x\cos^{2n_1}x\, dx & \displaystyle =\int (\sin^2 x)^{m_1}\cos^{2n_1} x \sin x\, dx \\ & \displaystyle =\int (1-\cos^2 x)^{m_1}\cos^{2n_1}x \sin x\, dx.
\end{array}
$$
Seguidamente si desarrollamos $(1-\cos^2 x)^{m_1}$ nos van saliento integrales del tipo $\displaystyle \int \cos^j x\sin x\, dx$, que son inmediatas, ver apartado 1.1.

## Integrales indefinidas de $\sin^m x\cos^n x$

**2.2: $m$ par y $n$ impar**. En este caso, existen dos naturales más, $m_1$ y $n_1$ tal que $m=2m_1$ y $n=2n_1+1$. Para resolver la integral inmediata, hacemos lo siguiente:
$$
\begin{array}{rl}
\displaystyle\int \sin^{2m_1}x\cos^{2n_1+1}x\, dx & \displaystyle =\int \sin^{2m_1}x (\cos^2 x)^{n_1} x \cos x\, dx \\ & \displaystyle =\int \sin^{2m_1}x (1-\sin^2 x)^{n_1} \cos x\, dx.
\end{array}
$$
Seguidamente si desarrollamos $(1-\sin^2 x)^{n_1}$ nos van saliento integrales del tipo $\displaystyle \int \sin^j x\cos x\, dx$ que son inmediatas, ver apartado 1.2.


## Integrales indefinidas de $\sin^m x\cos^n x$
* 3: Las dos potencias $m$ y $n$ son pares. En este caso, existen dos naturales más, $m_1$ y $n_1$ tal que $m=2m_1$ y $n=2n_1$. Para resolver la integral inmediata, hacemos lo siguiente:
$$
\begin{array}{rl}
\displaystyle\int \sin^{2m_1}x\cos^{2n_1}x\, dx & \displaystyle =\int (\sin^2 x)^{m_1}\cos^{2n_1} x \, dx \\ & \displaystyle =\int \left(\frac{1-\cos(2x)}{2}\right)^{m_1}\cdot\left(\frac{1+\cos (2x)}{2}\right)^{n_1}\, dx \\ & \displaystyle =\frac{1}{2^{m_1+n_1+1}}\int (1-\cos t)^{m_1}\cdot (1+\cos t)^{n_1}\, dt
\end{array}
$$
En la última igualdad hemos hecho el cambio de variable $t=2x$. 


## Integrales indefinidas de $\sin^m x\cos^n x$
Si desarrollamos las expresiones $(1-\cos t)^{m_1}\cdot (1+\cos t)^{n_1}$ nos quedarán sumas de integrales del tipo $\displaystyle \int \cos^j t\, dx$ que ya han sido estudiadas en los apartados 1.2 y 1.3. 

## Integrales indefinidas de $\sin^m x\cos^n x$

* 4: Las dos potencias $m$ y $n$ son impares. En este caso, existen dos naturales más, $m_1$ y $n_1$ tal que $m=2m_1+1$ y $n=2n_1+1$. Para resolver la integral inmediata, hacemos lo siguiente:
$$
\begin{array}{rl}
\displaystyle\int \sin^{2m_1+1}x\cos^{2n_1+1}x\, dx & \displaystyle =\int \sin^{2m_1+1}x (\cos^2 x)^{n_1} \cos x\, dx \\ & \displaystyle =\int \sin^{2m_1+1}x (1-\sin^2 x)^{n_1} \cos x\, dx.
\end{array}
$$

A continuación, si desarrollamos la expresión $(1-\sin^2 x)^{n_1}$ nos quedará una suma de integrales de la forma $\displaystyle\int \sin^j x\cos x\, dx$, con $j$ natural. Dichas integrales son inmediatas, ver apartado 1.2.

 
## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
Vamos a ver cómo se calculan las integrales indefinidas del tipo $\displaystyle\int \tan^n x\, dx$ y $\displaystyle\int\cot^n x\, dx$.

En primer lugar, calculemos las integrales anteriores para $n=1$ y $n=2$.

La integral $\displaystyle\int\tan x\, dx=\int\frac{\sin x}{\cos x}\, dx =-\int\frac{-\sin x}{\cos x}\, dx$ es inmediata y corresponde a la segunda fila de la tabla de integrales inmediatas con $g(x)=\cos x$:

$$
\int\tan x\, dx =-\ln |\cos x|+C.
$$

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
La integral $\displaystyle\int\cot x\, dx=\int\frac{\cos x}{\sin x}\, dx$ es inmediata y corresponde a la segunda fila de la tabla de integrales inmediatas con $g(x)=\sin x$:

$$
\int\cot x\, dx =\ln |\sin x|+C.
$$

Usando que la derivada de la función $\tan x$ vale $(\tan x)'=\frac{1}{\cos^2 x}=1+\tan^2 x$, la integral indefinida $\displaystyle\int \tan^2 x\, dx$ es sencilla de calcular:

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
$$
\begin{array}{rl}
\displaystyle\int \tan^2 x\, dx  & =\displaystyle\int (1+\tan^2 x-1)\, dx = \int (1+\tan^2 x)\, dx-\int 1\, dx \\ & \displaystyle =\tan x-x+C.
\end{array}
$$
De la misma manera, la integral de $\displaystyle\int \cot^2 x\, dx$ se puede calcular usando que $(\cot x)'=-\frac{1}{\sin^2 x}=-(1+\cot^2 x)$:
$$
\begin{array}{rl}
\displaystyle\int \cot^2 x\, dx  & \displaystyle =-\int -(1+\cot^2 x-1)\, dx \\ & \displaystyle = -\int -(1+\cot^2 x)\, dx - \int 1\, dx  =-\cot x-x+C.
\end{array}
$$

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
Sea un $n\geq 3$ natural. La integral indefinida $\displaystyle\int \tan^n x\, dx$ se calcularía de la forma siguiente:
$$
\begin{array}{rl}
\displaystyle\int\tan^n x\, dx & \displaystyle = \int\tan^{n-2} x (1+\tan^2 x-1)\, dx \\ & \displaystyle = \int\tan^{n-2} x (1+\tan^2 x)\, dx-\int \tan^{n-2} x\, dx
\end{array}
$$

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
La integral $\displaystyle \int\tan^{n-2} x (1+\tan^2 x)\, dx$ es inmediata y corresponde a la primera fila de la tabla de integrales inmediatas con $g(x)=\tan x$:
$$
\int\tan^{n-2} x (1+\tan^2 x)\, dx =\frac{\tan^{n-1} x}{n-1}+C.
$$
En resumen, hemos reducido el cálculo de la integral $\displaystyle\int \tan^n x\, dx$ al cálculo de la integral $\displaystyle\int \tan^{n-2} x\, dx$. 

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
Aplicando la técnica anterior unas $\frac{n}{2}$ veces, llegaríamos a la integral $\displaystyle\int \tan x\, dx$ o $\displaystyle\int\tan^2 x\, dx$ dependiendo de la paridad de $n$. El valor de dichas integrales ya ha sido calculado.

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$

Para calcular $\displaystyle\int \cot^n x\, dx$, usamos una técnica parecida:
$$
\begin{array}{rl}
\displaystyle\int\cot^n x\, dx & \displaystyle = -\int\cot^{n-2} x (-1-\cot^2 x+1)\, dx \\ & \displaystyle = -\int\cot^{n-2} x (-1-\cot^2 x)\, dx-\int \cot^{n-2} x\, dx
\end{array}
$$

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
La integral $\displaystyle \int\cot^{n-2} x (-1-\cot^2 x)\, dx$ es inmediata y corresponde a la primera fila de la tabla de integrales inmediatas con $g(x)=\cot x$:
$$
\int\cot^{n-2} x (-1-\cot^2 x)\, dx =\frac{\cot^{n-1} x}{n-1}+C.
$$
En resumen, hemos reducido el cálculo de la integral $\displaystyle\int \cot^n x\, dx$ al cálculo de la integral $\displaystyle\int \cot^{n-2} x\, dx$. 

## Integrales indefinidas de $\tan^n x$ y $\cot^n x$
Aplicando la técnica anterior unas $\frac{n}{2}$ veces, llegaríamos a la integral $\displaystyle\int \cot x\, dx$ o $\displaystyle\int\cot^2 x\, dx$ dependiendo de la paridad de $n$. El valor de dichas integrales ya ha sido calculado.

## Integrales indefinidas de $\sin(mx)\cos(nx)$
Para resolver dichas integrales consideraremos 3 casos:

* $\displaystyle\int\sin(mx)\sin(nx)\, dx$. Usando la fórmula que transforma el producto de funciones trigonométricas en sumas, obtenemos lo siguiente:

$$
\begin{array}{rl}
\displaystyle\int\sin(mx)\sin(nx)\, dx &  =\displaystyle  \frac{1}{2}\int (\cos((m-n)x)-\cos((m+n)x))\, dx\\
& = \displaystyle \frac{1}{2}\left(\frac{\sin((m-n)x)}{m-n}-\frac{\sin((m+n)x)}{m+n}\right)+C,
\end{array}
$$

si $m\neq n$.

## Integrales indefinidas de $\sin(mx)\cos(nx)$
Si $m=n$:
$$
\int\sin^2(nx)\, dx   = \frac{1}{2}\int (1-\cos(2nx))\, dx
 =  \frac{1}{2}\left(x-\frac{\sin (2nx)}{2n}\right)+C.
$$

## Integrales indefinidas de $\sin(mx)\cos(nx)$

* $\displaystyle\int\sin(mx)\cos(nx)\, dx$. Usando la fórmula que transforma el producto de funciones trigonométricas en sumas, obtenemos lo siguiente:
$$
\begin{array}{rl}
\displaystyle\int\sin(mx)\cos(nx)\, dx &  =\displaystyle  \frac{1}{2}\int (\sin((m-n)x)+\sin((m+n)x))\, dx\\
& = \displaystyle \frac{1}{2}\left(-\frac{\cos((m-n)x)}{m-n}-\frac{\cos((m+n)x)}{m+n}\right)+C,
\end{array}
$$
si $m\neq n$.

Si $m=n$:
$$
\int\sin(nx)\cos(nx)\, dx   = \frac{1}{2}\int \sin(2nx)\, dx
 =  -\frac{1}{4n}\cos (2nx)+C.
$$

## Integrales indefinidas de $\sin(mx)\cos(nx)$

* $\displaystyle\int\cos(mx)\cos(nx)\, dx$. Usando la fórmula que transforma el producto de funciones trigonométricas en sumas, obtenemos lo siguiente:
$$
\begin{array}{rl}
\displaystyle\int\cos(mx)\cos(nx)\, dx &  =\displaystyle  \frac{1}{2}\int (\cos((m-n)x)+\cos((m+n)x))\, dx\\
& = \displaystyle \frac{1}{2}\left(\frac{\sin((m-n)x)}{m-n}+\frac{\sin((m+n)x)}{m+n}\right)+C,
\end{array}
$$
si $m\neq n$.

Si $m=n$:
$$
\int\cos^2(nx)\, dx   = \frac{1}{2}\int (1+\cos(2nx))\, dx
 =  \frac{1}{2}\left(x+\frac{\sin (2nx)}{2n}\right)+C.
$$

## Integrales indefinidas de $R(\sin x, \cos x)$
En esta sección, vamos a dar un método para resolver integrales trigonométricas racionales del tipo $R(\sin x,\cos x)=\frac{P(\sin x,\cos x)}{Q(\sin x,\cos x)}$ donde $P$ y $Q$ son dos polinomios en las variable $\sin x$ y $\cos x$.

Para resolver este tipo de integrales, hemos de realizar el cambio de variable general $t=\tan\left(\frac{x}{2}\right)$.

Veamos cómo se transforman $\sin x$ y $\cos x$ como funciones de $t$.

En primer lugar, usando que $1+\tan^2\left(\frac{x}{2}\right)=\frac{1}{\cos^2\left(\frac{x}{2}\right)}$, deducimos que
$\cos^2\left(\frac{x}{2}\right)=\frac{1}{1+\tan^2\left(\frac{x}{2}\right)}=\frac{1}{1+t^2}$.

## Integrales indefinidas de $R(\sin x, \cos x)$
A continuación, usando que $\cos^2\left(\frac{x}{2}\right)=\frac{1+\cos x}{2}=\frac{1}{1+t^2}$, deducimos que 
$\cos x=\frac{1-t^2}{1+t^2}$.

De la misma manera, $\sin x=2\sin\left(\frac{x}{2}\right)\cos \left(\frac{x}{2}\right)=2\tan\left(\frac{x}{2}\right)\cos^2\left(\frac{x}{2}\right)=\frac{2t}{1+t^2}$.

La relación entre los diferenciales será la siguiente:
$$
dt = \frac{1}{2\cos^2 \left(\frac{x}{2}\right)}\, dx=\frac{\left(1+\tan^2\left(\frac{x}{2}\right)\right)}{2}dx = \frac{1+t^2}{2}dx\ \Rightarrow dx=\frac{2 dt}{1+t^2}.
$$

## Integrales indefinidas de $R(\sin x, \cos x)$
Después de realizar el cambio, la integral indefinida nos quedará, en función de la nueva variable $t$:
$$
\int R(\sin x,\cos x)\, dx = \int R\left(\frac{2t}{1+t^2},\frac{1-t^2}{1+t^2}\right)\frac{2 dt}{1+t^2}.
$$
Se trata de la integral indefinida de una función racional en $t$ que ya hemos estudiado.

El cambio que hemos propuesto nos sirve para resolver cualquier integral racional en $\sin x$ y $\cos x$. 

## Integrales indefinidas de $R(\sin x, \cos x)$
El problema es que la integral racional que nos sale, en muchas ocasiones, tiene el término $(1+t^2)^k$ con $k\geq 2$ en el denominador. Esto obliga a que tengamos que aplicar el método de Ostrogradski haciendo que el cálculo de la integral sea muy tedioso.

En algunas ocasiones, si la función $R$ verifica una cierta condición, podemos realizar otro cambio para transformar nuestra integral $\displaystyle \int R(\sin x,\cos x)\, dx$ en una integral racional más simple. Veamos a continuación en qué casos podemos hacer estos cambios más sencillos indicando dichos cambios.

## Integrales indefinidas de $R(\sin x, \cos x)$

* Supongamos que la función $R$ es par en las variables $\sin x$ y $\cos x$: $R(\sin x, \cos x)=R(-\sin x, -\cos x)$.
Entonces, sólo nos pueden salir potencias pares en $\sin x$ y $\cos x$.

En este caso hacemos el cambio $t=\tan x$, con $\cos^2 x=\frac{1}{1+t^2}$, $\sin^2 x=\frac{t}{1+t^2}$, $dx=\frac{dt}{1+t^2}$.

## Integrales indefinidas de $R(\sin x, \cos x)$

* Supongamos que la función $R$ es impar en la variable $\sin x$: $R(\sin x, \cos x)=-R(-\sin x, \cos x)$.
Entonces, sólo nos pueden salir potencias impares en $\sin x$.

En este caso hacemos el cambio $t=\cos x$, con $\sin x = \sqrt{1-t^2}$, $dx=-\frac{dt}{\sqrt{1-t^2}}$.

## Integrales indefinidas de $R(\sin x, \cos x)$
* Supongamos que la función $R$ es impar en la variable $\cos x$: $R(\sin x, \cos x)=-R(\sin x, -\cos x)$.
Entonces, sólo nos pueden salir potencias impares en $\cos x$.

En este caso hacemos el cambio $t=\sin x$, con $\cos x = \sqrt{1-t^2}$, $dx=\frac{dt}{\sqrt{1-t^2}}$.


# Integrales que contienen $\sqrt{ax^2+bx+c}$

## Introducción
En esta sección vamos a estudiar la integral indefinida de un conjunto de funciones que contienen la raíz cuadrada de un polinomio de segundo grado $\sqrt{ax^2+bx+c}$.

Concretamente, las integrales indefinidas que nos planteamos tienen la forma siguiente: $\displaystyle\int\frac{P(x)}{\sqrt{ax^2+bx+c}}\, dx$, donde $P(x)$ es un polinomio en la variable $x$.

Vamos a realizar el estudio del cálculo de la integral indefinida correspondiente dependiendo del signo del término principal $a$ y de si el polinomio $ax^2+bx+c$ tiene o no raíces reales.



## Caso $a>0$ y $b^2-4ac>0$
En este caso, la ecuación $a x^2+bx +c=0$ tiene dos raíces reales.

En primer lugar, "arreglamos" el término $\sqrt{ax^2+bx+c}$ de la siguiente manera:
$$
\begin{array}{rl}
\sqrt{ax^2+bx+c} & =\sqrt{a}\sqrt{x^2+\frac{b}{a}x+\frac{c}{a}}=\sqrt{a}\sqrt{\left(x+\frac{b}{2a}\right)^2+\frac{c}{a}-\frac{b^2}{4a^2}}\\ & = \sqrt{a}\sqrt{\left(x+\frac{b}{2a}\right)^2-\frac{b^2-4ac}{4a^2}}=\sqrt{\frac{b^2-4ac}{4a}}\sqrt{y^2-1},
\end{array}
$$
con $y=\frac{2a}{\sqrt{b^2-4 a c}}\left(x+\frac{b}{2a}\right)$.

## Caso $a>0$ y $b^2-4ac>0$
A continuación, nos planteamos el cambio de variable siguiente: $y=\sec t=\frac{1}{\cos t}$, o si se quiere:
$$
\frac{2a}{\sqrt{b^2-4 a c}}\left(x+\frac{b}{2a}\right)=\sec t=\frac{1}{\cos t}.
$$

La relación entre los diferenciales es la siguiente:
$$
\frac{2a}{\sqrt{b^2-4 a c}}\, dx=\frac{\sin t}{\cos^2 t}\, dt,\ \Rightarrow dx=\frac{\sqrt{b^2-4 a c}}{2a}\cdot \frac{\sin t}{\cos^2 t}\, dt.
$$

## Caso $a>0$ y $b^2-4ac>0$
El término $\sqrt{a x^2+bx+c}$ se nos transforma en función de la variable $t$ en:
$$
\begin{array}{rl}
\sqrt{a x^2+bx+c} & = \sqrt{\frac{b^2-4ac}{4a}}\sqrt{\frac{1}{\cos^2 t}-1}=\sqrt{\frac{b^2-4ac}{4a}}\frac{\sin t}{\cos t}\\ & =\sqrt{\frac{b^2-4ac}{4a}} \tan t.
\end{array}
$$

## Caso $a>0$ y $b^2-4ac>0$
De esta manera, hemos transformado la integral indefinida que contiene el término $\sqrt{a x^2+bx+c}$ en una integral racional en $\sin t$, $\cos t$, $\displaystyle\int R(\sin t,\cos t)\, dx$, que ya han sido estudiadas:
$$
\int\frac{P(x)}{\sqrt{ax^2+bx+c}}\, dx =\frac{1}{\sqrt{a}}\int \frac{P\left(\frac{\sqrt{b^2-4ac}}{2a\cos t}-\frac{b}{2a}\right)}{ \cos t}\, dt
$$


## Caso $a>0$ y $b^2-4ac<0$
En este caso, la ecuación $a x^2+bx +c=0$ no tiene raíces reales.

El "arreglo" del término $\sqrt{ax^2+bx+c}$ será, en este caso:
$$
\begin{array}{rl}
\sqrt{ax^2+bx+c} & =\sqrt{a}\sqrt{x^2+\frac{b}{a}x+\frac{c}{a}}=\sqrt{a}\sqrt{\left(x+\frac{b}{2a}\right)^2+\frac{c}{a}-\frac{b^2}{4a^2}}\\ & = \sqrt{a}\sqrt{\left(x+\frac{b}{2a}\right)^2+\frac{4 a c-b^2}{4a^2}}=\sqrt{\frac{4 a c-b^2}{4a}}\sqrt{y^2+1},
\end{array}
$$
con $y=\frac{2a}{\sqrt{4 a c-b^2}}\left(x+\frac{b}{2a}\right)$.

## Caso $a>0$ y $b^2-4ac<0$
A continuación, nos planteamos el cambio de variable siguiente: $y=\tan t$, o si se quiere:
$$
\frac{2a}{\sqrt{4 a c-b^2}}\left(x+\frac{b}{2a}\right)=\tan t.
$$

La relación entre los diferenciales es la siguiente:
$$
\frac{2a}{\sqrt{4 a c-b^2}}\, dx=\frac{1}{\cos^2 t}\, dt,\ \Rightarrow dx=\frac{\sqrt{4 a c-b^2}}{2a}\cdot \frac{1}{\cos^2 t}\, dt.
$$

## Caso $a>0$ y $b^2-4ac<0$
El término $\sqrt{a x^2+bx+c}$ se nos transforma en función de la variable $t$ en:
$$
\sqrt{a x^2+bx+c}  = \sqrt{\frac{4 a c-b^2}{4a}} \sqrt{\tan^2 t+1}=\sqrt{\frac{4 a c-b^2}{4a}}\frac{1}{\cos t}.
$$

De esta manera, hemos transformado la integral indefinida que contiene el término $\sqrt{a x^2+bx+c}$ en una integral racional en $\sin t$, $\cos t$, $\displaystyle\int R(\sin t,\cos t)\, dx$, que ya han sido estudiadas:
$$
\int\frac{P(x)}{\sqrt{ax^2+bx+c}}\, dx =\frac{1}{\sqrt{a}}\int \frac{P\left(\frac{\sqrt{4ac-b^2}\tan t}{2a}-\frac{b}{2a}\right)}{ \cos t}\, dt.
$$

## Caso $a<0$ y $b^2-4ac>0$
En este caso, la ecuación $a x^2+bx +c=0$ tiene dos raíces reales.

El "arreglo" del término $\sqrt{ax^2+bx+c}$ será, en este caso:
$$
\begin{array}{rl}
\sqrt{ax^2+bx+c} & =\sqrt{-a}\sqrt{-x^2-\frac{b}{a}x-  \frac{c}{a}}=\sqrt{-a}\sqrt{-\left(x+\frac{b}{2a}\right)^2-\frac{c}{a}+\frac{b^2}{4a^2}}\\ & = \sqrt{-a}\sqrt{-\left(x+\frac{b}{2a}\right)^2+\frac{b^2-4 a c}{4a^2}}=\sqrt{\frac{4 a c-b^2}{4a}}\sqrt{1-y^2},
\end{array}
$$
con $y=\frac{2|a|}{\sqrt{b^2-4 a c}}\left(x+\frac{b}{2a}\right)=\frac{-2 a}{\sqrt{b^2-4 a c}}\left(x+\frac{b}{2a}\right)$.

## Caso $a<0$ y $b^2-4ac>0$
A continuación, nos planteamos el cambio de variable siguiente: $y=\sin t$, o si se quiere:
$$
\frac{-2 a}{\sqrt{b^2-4 a c}}\left(x+\frac{b}{2a}\right) =\sin t.
$$

La relación entre los diferenciales es la siguiente:
$$
\frac{-2 a}{\sqrt{b^2-4 a c}}\, dx=\cos t\, dt,\ \Rightarrow dx=-\frac{\sqrt{b^2-4ac}}{2a}\cdot \cos t\, dt.
$$

## Caso $a<0$ y $b^2-4ac > 0$
El término $\sqrt{a x^2+bx+c}$ se nos transforma en función de la variable $t$ en:
$$
\sqrt{a x^2+bx+c}  = \sqrt{\frac{4 a c-b^2}{4a}} \sqrt{1-\sin^2 t}=\sqrt{\frac{4 a c-b^2}{4a}} \cos t.
$$

De esta manera, hemos transformado la integral indefinida que contiene el término $\sqrt{a x^2+bx+c}$ en una integral racional en $\sin t$, $\cos t$, $\displaystyle\int R(\sin t,\cos t)\, dx$, que ya han sido estudiadas:
$$
\int\frac{P(x)}{\sqrt{ax^2+bx+c}}\, dx =-\frac{1}{\sqrt{-a}}\int P\left(-\frac{\sqrt{b^2-4ac}\sin t}{2a}-\frac{b}{2a}\right)\, dt.
$$


## Caso $a<0$ y $b^2-4ac < 0$
En este caso, la ecuación $a x^2+bx +c=0$ no tiene raíces reales.

Este caso no tendría sentido considerarlo ya que para todo valor $x\in\mathbb{R}$ real, $ax^2+bx+c<0$. Por tanto, el dominio de la función $\sqrt{ax^2+bx+c}$ sería el conjunto vacío, $\emptyset$.

## Otras integrales indefinidas que contienen $\sqrt{ax^2+bx+c}$
Veamos otras integrales indefinidas donde se pueden aplicar las técnicas de integración vistas en esta sección.

Para calcular la integral indefinida del tipo $\displaystyle\int\frac{dx}{(e x+f)\sqrt{a x^2+b x+c}}\, dx$, donde $a,b,c,e$ y $f$ son constantes, podemos considerar el cambio siguiente:  $t=\frac{1}{e x+f}$.

## Otras integrales indefinidas que contienen $\sqrt{ax^2+bx+c}$
La relación entre los diferenciales es el siguiente: $dt=-\frac{e}{(ex+f)^2}\,dx=-e t^2\, dx$. Por tanto, $dx=-\frac{1}{e t^2}\, dt$. Entonces la integral en la nueva variable $t$ sería:
$$
\int\frac{dx}{(d x+e)\sqrt{a x^2+b x+c}} =-\int \frac{dt}{\sqrt{(a f^2-b e f+c e^2) t^2+(b e-2 a f)t+a}}.
$$
La última integral sería del tipo que hemos estudiado antes.

## Otras integrales indefinidas que contienen $\sqrt{ax^2+bx+c}$

Para calcular una integral indefinida del tipo $\displaystyle\int\sqrt{ax^2+bx+c}\, dx$, podemos realizar los cambios indicados en esta sección y quedarán transformadas en integrales trigonométricas del tipo $\displaystyle\int R(\sin x,\cos x)\, dx$ que ya han sido estudiadas.

# Integración de otras funciones racionales

## Introducción
En esta sección nos planteamos el cálculo de integrales indefinidas del tipo 
$$
\int R\left(x,\left(\frac{ax+b}{cx+e}\right)^{r_1},\left(\frac{ax+b}{cx+e}\right)^{r_2},\ldots, \left(\frac{ax+b}{cx+e}\right)^{r_k}\right)\, dx,
$$
donde $R$ es una función racional en las variables $x$, $\left(\frac{ax+b}{cx+e}\right)^{r_1},\ldots,\left(\frac{ax+b}{cx+e}\right)^{r_k}$, y los valores $r_i$ son valores racionales de la forma $r_i=\frac{p_i}{q_i}$, $i=1,\ldots,k$.

## Cambio de variable
Para el cálculo de integrales de este tipo, consideramos el cambio de variable siguiente: $t^n =\frac{ax+b}{cx+e}$, donde $n$ es el mínimo común múltiplo de los denominadores de los valores $r_i$: $n=\mathrm{mcm}(q_1,\ldots,q_k)$.

La relación entre los diferenciales es la siguiente:
$$
m t^{m-1}\, dt = \frac{ae-bc}{(cx+e)^2}\, dx\ \Rightarrow dx=\frac{(ae-bc) m t^{m-1}}{(c t^m-a)^2}\, dt.
$$
Sean los números naturales $\alpha_i = \frac{m p_i}{q_i}$, $i=1,\ldots, k$. Dichos números son naturales ya que como $m$ és múltiplo de $p_i$, $\frac{m}{q_i}\in\mathbb{N}$.

## Cambio de variable
El valor de la integral a calcular en la nueva variable $t$ sería:
$$
\int R\left(\frac{e t^m-b}{a-c t^m},t^{\alpha_1},t^{\alpha_2},\ldots, t^{\alpha_k}\right)\frac{(ae-bc) m t^{m-1}}{(c t^m-a)^2}\, dt.
$$
Se trataría de una integral racional en la variable $t$ y, por tanto, ya las sabemos resolver ya que han sido estudiadas anteriormente.
