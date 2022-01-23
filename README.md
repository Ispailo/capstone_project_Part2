# capstone_project_Part2
Docker Compose est un outil qui permet de décrire (dans un fichier YAML) et gérer (en ligne de commande) plusieurs conteneurs comme un ensemble de services inter-connectés. Si je travaille sur une application Rails, je vais par exemple décrire un ensemble composé de 3 conteneurs :

un conteneur PostgreSQL
un conteneur Redis
un conteneur pour le code de mon application
Je pourrai alors démarrer mon ensemble de conteneurs en une seule commande docker-compose up. Sans Docker Compose, j’aurais dû lancer 3 commandes docker run avec beaucoup d’arguments pour arriver au même résultat. Par ailleurs, cela aurait nécessité que je rédige un README plutôt précis pour que les autres membres de mon équipe obtiennent le même résultat. Avec Docker Compose, cette configuration est faite dans un fichier qui est versionné avec le reste du code de l’application.

Dans le fichier docker-compose.yml, chaque conteneur est décrit avec un ensemble de paramètres qui correspondent aux options disponibles lors d’un docker run : l’image à utiliser, les volumes à monter, les ports à ouvrir, etc. Mais on peut également y décrire des éléments supplémentaires, comme la possibilité de « construire » (docker build) une image à la volée avant d’en lancer le conteneur.

####################Partie 2 : Conteneuriser une application Node.js pour le développement avec Docker Compose####################

Ce tutoriel vous montrera comment configurer un environnement de développement pour une application Node.js à l'aide de Docker. Vous allez créer deux conteneurs — un pour l'application Node et un autre pour la base de données MongoDB — avec Docker Compose. Étant donné que cette application fonctionne avec Node et MongoDB, notre configuration effectuera les opérations suivantes :

  - Synchronisez le code de l'application sur l'hôte avec le code dans le conteneur pour faciliter les modifications lors du développement.
  - Assurez-vous que les modifications apportées au code de l'application fonctionnent sans redémarrage.
  - Créez une base de données protégée par un utilisateur et un mot de passe pour les données de l'application.
  - Persistez ces données.
  
 Pour la réalisation de cette partie j'ai suivi les étapes suivantes: 
 
  * Cloner le projet et modifier les dépendances
  * Configuration de votre application pour fonctionner avec des conteneurs
  * Modification des paramètres de connexion à la base de données
  * Définir des services avec Docker Compose
  * Tester l'application
  
  
![image](https://user-images.githubusercontent.com/80095967/150679645-4bae5835-17c6-4b80-9c6e-597e72769552.png)
![image](https://user-images.githubusercontent.com/80095967/150679670-e562f186-973b-4fdf-8354-b279f1ba0341.png)
![image](https://user-images.githubusercontent.com/80095967/150679682-130dfad0-8ae8-423a-b97d-885606df3db0.png)
