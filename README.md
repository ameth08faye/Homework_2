# Homework_2
#Exercice1

base_donnees1 <- data.frame(
  Identifiant = c(1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16),
  noms = c("MBB", "KC", "KD", "Diawa", "Bathie", "Hilda", "Ameth", "Sarah", "Célina", "Tam", "Salam", "NIASS", "Ange", "Jeanne", "Malick", "PAN"), 
  Sexe = factor(c("Homme", "Femme", "Femme", "Femme", "Homme", "Femme", "Homme", "Femme", "Femme", "Homme", "Homme", "Homme", "Homme", "Femme", "Homme", "Homme")),
  Nationalite = c("Sénégalaise", "Sénégalaise", "Sénégalaise", "Sénégalaise", "Sénégalaise", "Camerounaise", "Sénégalaise", "Camerounaise", "Camerounaise", "Sénégalaise", "Sénégalaise", "Sénégalaise", "Malgache", "Camerounaise", "Sénégalaise", "Sénégalaise"),
  Poids = c(69, 60, 62, 65, 67, 68, 72, 65, 65, 75, 70, 68, 67, 70, 70, 72)
)
View(base_donnees1)

# Vecteurs pour Identifiant et Poids
identifiant <- c(1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16)
poids <- c(69, 60, 62, 65, 67, 68, 72, 65, 65, 75, 70, 68, 67, 70, 70, 72)

# Création de la matrice avec les vecteurs
matrice_donnees <- matrix(c(identifiant, poids), ncol = 2, byrow = FALSE,
                          dimnames = list(NULL, c("Identifiant", "Poids")))

# Affichage de la matrice
print(matrice_donnees)

# Renommer les lignes avec des noms personnalisés
rownames(base_donnees1) <- paste0("Individu", 1:16)

# Affichage de la matrice avec les nouvelles lignes renommées
print(base_donnees1)

##Analyse univariée

#Statistiques descriptives sur le poids
summary(base_donnees1$Poids)

#Tri à plat
table(base_donnees1$Sexe)

#Histograme de la répartition par sexe à partir du tri à plat
tab <- table(base_donnees1$Sexe)
barplot(tab,main= "Répartition par sexe",xlab="Sexe",ylab="effectif",col="springgreen1")

# Créer un tableau de fréquence des nationalités
table_nationalites <- table(base_donnees1$Nationalite)

# Tracer un diagramme à barres
barplot(table_nationalites, main = "Répartition des Nationalités",
        xlab = "Nationalité", ylab = "Effectif", col = "skyblue")




#Exercice2
# Fonction objectif : f(x) = x^2 - 4x + 5
# Calcul de la dérivée première : f'(x) = 2x - 4
# Résolution de l'équation f'(x) = 0 pour trouver le minimum
# x_min = 2 (valeur qui minimise la fonction)

# Calcul de la valeur minimale de la fonction
x_min <- 2
f_min <- x_min^2 - 4*x_min + 5
cat("La valeur minimale de la fonction est f(x_min) =", f_min, "\n")
