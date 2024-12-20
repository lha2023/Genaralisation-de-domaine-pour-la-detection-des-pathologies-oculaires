# Commande Entreprise : Généralisation de Domaine pour la Détection des Pathologies Oculaires

Dans le cadre du projet "Commande Entreprise", nous avons travaillé sur la détection multi-pathologique à partir d'images de fond d'œil en utilisant plusieurs modèles de Deep Learning. Un défi majeur pour le client était la perte de précision du modèle lors du changement de source de données, un phénomène appelé "Domain Shift". Nous avons donc expérimenté différents algorithmes afin de déterminer lesquels seraient les plus adaptés pour résoudre ce problème.

## Prétraitement des Données

Au cours du projet, nous avons effectué un prétraitement approfondi des données, reflété dans l'analyse statistique. Les bases de données que nous avons utilisées incluent ODIR, RIADD et Kaggle DR+. Le code de prétraitement des données est disponible dans le dossier `Statistique`.

## Utilisation des Modèles

### RetFound
- **Finetuning de toutes les couches** : Le notebook fourni permet de télécharger les données depuis le site du client (avec des liens configurables), de récupérer les labels dans le dossier `CSV_files`, et de formater les données pour les rendre compatibles avec les exigences d'entrée de RetFound.

- **Finetuning de la couche dense** : Pour effectuer cette tâche, il est nécessaire de modifier certaines lignes de code dans le repository GitHub, ce qui permettra de ne mettre à jour que les poids de la couche dense. Les codes nécessaires pour cela sont disponibles dans le dossier `RetFound`.

### Resnet_Fisher
- **Création de class Riad et Odir** : Le notebook permet de se connecter avec le drive ou' vous devez déposer les images et les csv. Ou, vous pouvez avoir accès au Drive pour pouvoir accéder facilement.


- **Entrainement du modèle** : Le notebook permet aussi d'entrainer le modèle qui est un resnet50 plus un classifier pour pouvoir faire de la prédiction. Une fois le modèle est entrainé sur Riad. Une autre fois il est entrainé sur les deux base de données à l'aide de fishr. J'ai mis le lien vers les modèles déja entrainnés.


- **Plot** : Il y'a aussi un code qui permet de tracer la valeur d'AUC par classe et aussi la valeur moyenne.
### BiomedClip

- **Zero-shot** : Une première version de zero-shot est disponible afin d'avoir un exemple du foncionnement. L'évaluation n'est pas disponible dans ce code.

- **Fine tuning**: une tentative de finetuning est disponible, mais s'est soldé par un echec
