# Introduction
L’échantillonnage numérique de distributions de probabilité a des applications
importantes dans l’apprentissage automatique, l’intelligence artificielle et les statis-
tiques computationnelles.
À titre d’exemple en inférence bayesienne, on a besoin d’avoir la distribution des
paramètres qui va nous permettre de calculer la distribution postérieure prédictive.
Soit π la distribution cible. Pour ce faire, on va introduire des fonctions de dissimi-
larité qui peuvent donc être utilisées pour approximer π, puisque, sous de légères
hypothèses, elles ne s’annulent que pour μ = π.
Parmi ces fonctions de dissimilarité, on peut citer la Kernel Stein Discrepancy puis-
qu’elle peut être facilement calculée lorsque on a accès au score de π, et pour une
distribution μ discrète.
Alors grâce à cette fonction, on peut partir d’une distribution quelconque de parti-
cules et appliquer un schéma de descente permettant de converger vers la distribution
cible, en l’optimisant sur μ. En particulier, on peut considérer le flot de gradient de
Wasserstein. Ce dernier peut être interprété comme un champ de vecteurs déplaçant
continuellement les particules supportant μ vers la distribution cible.
Pour cela, on va introduire l’algorithme de KSD descent qui permet d’effectuer cette
tâche, étudier ses limites, le comparer avec d’autres méthodes d’inférence variation-
nelle, et essayer de l’améliorer grâce à d’autres processus comme le processus de
naissance mort.
