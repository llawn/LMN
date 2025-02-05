#Topologie #Compact #Compacité
# Quasi-compact
Soit $(X,T)$ un [[espace topologique]], $X$ est dit **quasi-compact** s'il vérifie la propriété de [[#Borel-Lebesgue]].

Une partie $K \subset X$ est dite **quasi-compacte** si elle est quasi-compacte pour sa topologie induite.
## Borel-Lebesgue
De tout recouvrement de X par des [[Espace topologique#Ouverts|ouverts]], on peut extraire un sous-recouvrement fini:  
$$
\forall (O_i)_{i \in I} \in T^I,  \text{tel que } \bigcup_{i \in I} O_i = X, \exists J \subset I, |J| < +\infty, \text{tel que } \bigcup_{j \in J} O_j = X
$$
Par passage au complémentaire, la propriété équivaut à:

$$
\forall (F_i)_{i \in I} \text{ ferm\'es},  \text{tel que } \bigcap_{i \in I} F_i = \emptyset, \exists J \subset I, |J| < +\infty, \text{tel que } \bigcap_{j \in J} F_j = \emptyset
$$
# Compact
## Espace topologique
Soit $(X,T)$ un [[espace topologique]], $K \subset X$ est dit **compact** s'il est  [[#quasi-compact]] et [[Espace séparé|séparé]].
## Espace métrique
Soit $(X,d)$ un [[espace métrique]], $K \subset X$ est **compact** si et seulement si il vérifie la propriété de [[#Bolzano-Weierstrass]]:
### Bolzano-Weierstrass
De toute suite d'éléments de $K$, on peut extraire une sous-suite convergente dans $K$.
