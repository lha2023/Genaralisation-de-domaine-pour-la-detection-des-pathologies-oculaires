# Commande Entreprise : Généralisation de Domaine pour la Détection des Pathologies Oculaires

Dans le cadre du projet "Commande Entreprise", nous avons travaillé sur la détection multi-pathologique à partir d'images de fond d'œil en utilisant plusieurs modèles de Deep Learning. Un défi majeur pour le client était la perte de précision du modèle lors du changement de source de données, un phénomène appelé "Domain Shift". Nous avons donc expérimenté différents algorithmes afin de déterminer lesquels seraient les plus adaptés pour résoudre ce problème.

## Prétraitement des Données

Au cours du projet, nous avons effectué un prétraitement approfondi des données, reflété dans l'analyse statistique. Les bases de données que nous avons utilisées incluent ODIR, RIADD et Kaggle DR+. Le code de prétraitement des données est disponible dans le dossier `Statistique`.

## Utilisation des Modèles

### RetFound
- **Finetuning de toutes les couches** : Le notebook fourni permet de télécharger les données depuis le site du client (avec des liens configurables), de récupérer les labels dans le dossier `CSV_files`, et de formater les données pour les rendre compatibles avec les exigences d'entrée de RetFound.
