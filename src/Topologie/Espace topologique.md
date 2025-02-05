#Topologie #Convergence #Limite
# Definition
Un espace topologique $(X,\mathcal{T})$ où $X$ est un ensemble et $T\in \mathcal{P}(X)$ une topologie sur $X$ vérifiant:

1. $\emptyset, X \in \mathcal{T}$
2. Toute réunion *quelconque* d'ouverts est un ouvert
	$$ \forall (O_i)_{i \in I} \in \mathcal{T}^I, \bigcup_{i \in I} O_i \in \mathcal{T}$$
3. Toute intersection *finie* d'ouverts est un un ouvert
	$$ \forall (O_j)_{j \in J} \in \mathcal{T}^J, |J| < +\infty, \bigcap_{j \in I} O_j \in \mathcal{T}$$
De manière équivalente, on peut remplacer 3. par:
$$\forall U,V \in \mathcal{T}, U \cap V \in \mathcal{T}$$
## Ouvert
Les éléments d'une [[#Definition|topologie]] sont les **ouverts**.
### Topologie Induite
Soit $A \subset X$, les ouverts de $A$ sont les $A \cap O$ pour $O \in \mathcal{T}$.
Les ouverts de A forment une [[#Definition|topologie]] sur A appelée **topologie induite**.
## Fermé
Les **fermés** sont les complémentaires des [[#Ouvert|ouverts]].
$$
F \text{ ferm\'e} \underset{def}{\Longleftrightarrow} F^c \text{ ouvert}
$$
## Comparaison de topologie
Soient $\tau_1, \tau_2$ deux topologies sur $X$.
On dit que $\tau_2$ est **plus fine** que $\tau_1$ (ou que $\tau_1$ est **moins fine** que $\tau_2$) noté $\tau_1 \subseteq \tau_2$ lorsque:
$$\tau_1 \subseteq \tau_2 \underset{def}{\Longleftrightarrow} \forall O \subset X, O \in \tau_1 \Rightarrow O \in \tau_2$$
## Topologie Discrète
Il s'agit de $(X,\mathcal{P}(X))$. C'est la topologie la [[#Comparaison de topologie|plus fine]] sur X.
## Topologie Grossière
Il s'agit de $(X,\{\emptyset,X\})$. C'est la topologie la [[#Comparaison de topologie|moins fine]] sur X.
## Topologie Produit
Soit $(X_i, \mathcal{T}_i)_{i \in I}$ des espaces topologiques *($I$ quelconque).
### Cylindre ouvert
Soit $J \subset I$, $J=\{j_i, \ldots, j_n\}$ fini et $\Omega_{j_k} \in \mathcal{T}_{j_k}$. On appelle **cylindre ouvert** de base $(\Omega_j)_{j \in J}$ l'ensemble
$$
\mathrm{Cyl}(\Omega_{j_1}, \ldots, \Omega_{j_n}) = \prod_{i\in I}Y_{i},
\quad \text{avec} \quad 
Y_{i} = 
   \left\{\begin{array}{l}
      \Omega_{i} \quad \text{si} \quad i \in J, \\
      X_{i} \quad \text{sinon}
\end{array}\right. 
$$
### Topologie produit
La **topologie produit** sur $X=\prod_{i\in I}X_{i}$ notée $\prod_{i\in I}\mathcal{T}_{i}$ est la topologie de base
$$
\{
   \mathrm{Cyl}(\Omega_{j_1}, \ldots, \Omega_{j_n}) \quad | \quad
   n \in \mathbb{N}^*, \forall k \in [n], j_k \in I, \Omega_{j_k}\in \mathcal{T}_{j_k} 
\}
$$
## Topologie Métrique
Si $(X,d)$ est un [[espace métrique]] le topologie métrique $\mathcal{T}_d$ est définie par
$$ O \in \mathcal{T}_d
\Longleftrightarrow
\forall x \in O, \exists r > 0 \text{ tq } B(x,r) \subset O
$$
# Voisinage
Soient $x \in X$ et $V \subset X$. On dit  que $V$ est un **voisinage** $x$ noté $V\in \mathcal{V}(x)$ lorsque:
$$
V\in \mathcal{V}(x)
\underset{def}{\Longleftrightarrow}
\exists O \in \mathcal{T},x \in O \text{ et } O \subset V
$$
# Limite
Soient $(u_n)_n \in X^\mathbb{N}$ et $\ell \in X$, on a:
$$
\underset{n \to \infty}{lim} u_n = \ell 
\underset{def}{\Longleftrightarrow}
\forall V \in \mathcal{V}(\ell), \exists N \in \mathbb{N}, \forall n \in \mathbb{N}, n \ge N \Rightarrow  u_n \in V
$$
**Remarques**:
- Il n'y a pas unicité de la limite dans un espace topologique quelconque mais dans un [[espace métrique]].
# Adhérence
## Point adhérent
Soient $A \subset X$ et $x \in X$, on dit que a est un **point  adhérent** lorsque
$$
\forall V \in \mathcal{V}(x), V \cap A \neq \emptyset
$$
## Adhérence
L'ensemble des [[#Point adhérent|points adhérents]] à $A \subset X$ est l'**adhérence** de A noté $\mathrm{Adh}(A)$ ou $\bar{A}$.

**Caractérisation**
L'**adhérence** de A est le plus petit [[#fermé]] contenant A:
$$
\forall F \text{ ferm\'e}, A \subset F \Rightarrow \bar{A} \subset F
$$
**Propriétés**
- $\forall A,B \subset X, \overline{A \cap B} \subset \bar{A} \cap \bar{B}$
- $\forall A,B \subset X, \overline{A \cup B} = \bar{A} \cup \bar{B}$
- $\forall (u_n)_n \in A^\mathbb{N}, \forall x \in X, \mathrm{lim} u_n = x \Rightarrow x \in \bar{A}$
	Réciproque vraie dans un [[espace métrique]]
# Point isolé
Soient $A \subset X$ et $a \in A$, on dit que $a$ est un **point isolé** de A lorsque
$$\exists O \in \mathcal{T}, O \cap A = \{a\}$$
Ce qui équivaut à dire que $\{a\}$ est un [[#ouvert]] de A (pour la [[#topologie Induite]]).

## Ensemble discret
$A \subset X$ est un ensemble **discret** si et seulement si tous les points de $A$ sont [[#Point isolé|isolés]].
# Point d'accumulation
Soient $A \subset X$ et $a \in A$, on dit que $a$ est un **point d'accumulation** de A lorsque
$$\forall V \in \mathcal{V}(a), V \setminus \{a\} \cap A \neq \emptyset $$
# Intérieur
## Point intérieur
Soient $A \subset X$ et $x \in X$ On dit que $x$ est un **point intérieur** de A si et seulement si $A \in \mathcal{V}(x)$.
## Intérieur
L'ensemble des [[#Point intérieur|points intérieurs]] de $A$ s'appelle l'**intérieur** de $A$ noté $\mathring{A}$.

**Caractérisation**
L'**intérieur** de A est le plus grand [[#ouvert]] inclus dans A:
$$
\forall O \in \mathcal{T}, O \subset A \Rightarrow O \subset \mathring{A}
$$
**Propriétés**
- $\overline{A^c}=\left(\mathring{A}\right)^c$
-  $\forall A,B \subset X, \mathring{A \cap B} = \mathring{A} \cap \mathring{B}$
- $\forall A,B \subset X, \mathring{A} \cup \mathring{B} \subset \mathring{A \cup B}$
# Frontière
On appelle **frontière** de A $\mathrm{Fr}(A)=\partial A=\bar A \setminus \mathring{A}$
