---
title: Projets
showDate: false
showReadingTime: false
showWordCount: false
showAuthor: false
---
<style>
  header.relative.flex.flex-col, 
  .relative.flex.flex-col.items-center.justify-center {
      display: none !important;
  }

  article {
      margin-top: 140px !important; 
  }
 
.grid-cols-2, 
.pagination,
.post-navigation {
    display: none !important;
}


footer {
    display: none !important;
    height: 0 !important;
    padding: 0 !important;
    margin: 0 !important;
}


hr {
    display: none !important;
}
</style>

# 📚 Projet 1: MediaTek86

Le projet MediaTek86 est une application web complète développée avec le framework Symfony 5.4. Son but principal est de centraliser et de structurer un catalogue de formations en ligne, principalement sous forme de tutoriels vidéo, pour faciliter l'auto-formation des collaborateurs ou des utilisateurs. Il est disponible dans ce dépôt [**Github**](https://github.com/Giovanni2626/Application-Symfony).

Voici le détail du projet :

## 🛠️ Technologies Utilisées
* **Langage :** PHP 8.1
* **Framework :** Symfony 5.4 (Architecture MVC)
* **Gestion de données :** MySQL & Doctrine ORM
* **Outils :** Visual Studio Code, WAMP/MAMP, Git/GitHub, AlwaysData (Déploiement)
* **Dépendances :** Composer, Symfony CLI

### 🏗️ La Genèse et l'Architecture
Le projet repose sur une architecture MVC (Modèle-Vue-Contrôleur), ce qui permet de bien séparer la logique de données, l'affichage et la gestion des requêtes.

* **Le Backend (PHP 8.1 / Symfony)** : Il gère toute la communication avec la base de données MySQL via l'ORM Doctrine. C'est ici que sont définies les relations entre les formations, les playlists et les catégories.
* **Le Frontend (Twig / Bootstrap)** : L'interface utilisateur est construite avec le moteur de template Twig, permettant d'afficher dynamiquement les données, tandis que Bootstrap assure une présentation propre et professionnelle.

### 🔍 Le Système de Consultation et de Filtrage
L'une des parties les plus complexes du projet a été de créer un système de recherche intuitif. Pour éviter que l'utilisateur ne se perde dans une liste interminable, nous avons mis en place :

* **Des tris multicritères** : L'utilisateur peut trier les formations par titre ou par date, et les playlists par nom ou par nombre de formations contenues.
* **Des filtres par colonnes** : Chaque colonne du tableau (Formation, Playlist, Catégorie) possède son propre formulaire de recherche. 

### 🔐 L'Espace Administration (Backoffice)
Le projet intègre une gestion stricte des droits d'accès.

* **Sécurisation** : Alors que les visiteurs peuvent seulement consulter les vidéos, un administrateur doit se connecter pour accéder aux fonctionnalités de modification.
* **Gestion du contenu (CRUD)** : L'administrateur peut Créer une nouvelle formation, Lire (visualiser) les détails, Mettre à jour (modifier le titre, la description ou la vidéo) et Supprimer les éléments obsolètes. Cette gestion s'étend aussi aux catégories et aux playlists pour garder un catalogue organisé.

### 📱 L'Optimisation pour Mobile (Responsive Design)
Un point d'honneur a été mis sur l'accessibilité sur tous les supports.

* **Navigation adaptative** : Nous avons intégré un menu "hamburger" (bouton toggler) qui cache les liens de navigation sur mobile pour ne pas encombrer l'écran, tout en restant accessible d'un simple clic.


### 🌐 Déploiement et Mise en Production
Enfin, le projet a été configuré pour être déployé sur un serveur distant (AlwaysData). Cela a nécessité une gestion rigoureuse du cache de Symfony. En mode production, le framework compile les fichiers Twig pour gagner en rapidité, ce qui demande de vider manuellement le cache à chaque mise à jour du code pour que les changements visuels soient visibles par tous les internautes.

## 📸 Aperçu du site

![Capture Ecran](/accueil.png)
![Capture Ecran](/formationsdeconnecter.png)
![Capture Ecran](/playlistsdeconnecter.png)
![Capture Ecran](/connexion.png)
![Capture Ecran](/formations.png)
![Capture Ecran](/ajouterformation.png)
![Capture Ecran](/ajouterformationmessage.png)
![Capture Ecran](/modifierformation.png)
![Capture Ecran](/modifierformationmessage.png)
![Capture Ecran](/supprimerformationmessage.png)
![Capture Ecran](/playlists.png)
![Capture Ecran](/ajouterplaylist.png)
![Capture Ecran](/ajouterplaylistmessage.png)
![Capture Ecran](/modifierplaylist.png)
![Capture Ecran](/modifierplaylistmessage.png)
![Capture Ecran](/supprimerplaylistmessage.png)
![Capture Ecran](/ajoutercatégorie.png)
![Capture Ecran](/ajoutercatégoriemessage.png)
![Capture Ecran](/supprimercatégoriemessage.png)


# 📚 Projet 2: MediaTekDocuments 

MediaTekDocuments est une application de bureau développée en **C#** permettant de gérer le catalogue et les commandes d'une médiathèque (livres, DVD, revues). 

L'application repose sur une architecture **n-tiers**, communiquant avec une base de données MySQL via une **API REST** sécurisée. L'app est disponible sur ce dépôt [**Github**](https://github.com/Giovanni2626/MediaTekDocuments) et l'API sur ce dépôt [**Github**](https://github.com/Giovanni2626/rest_mediatekdocuments).


## 🛠️ Technologies Utilisées
* **Langage :** C# (.NET Framework)
* **Interface :** Windows Forms (WinForms)
* **Gestion de données :** API REST (PHP / Slim Framework) & MySQL
* **Outils :** Visual Studio, WAMP, Postman, Git/GitHub
* **Dépendances :** Newtonsoft.Json, Composer, Dotenv

## 🚀 Missions Réalisées

###  Gestion des Commandes et Suivi (Livre/DVD)
* Implémentation du cycle de vie des commandes : *En cours, Relancée, Livrée, Réglée*.
* Automatisation de la création des exemplaires physiques en base de données lors de la réception des commandes.
* Contrôle strict des transitions d'états pour garantir l'intégrité des processus d'achat.

###  Gestion des Abonnements (Revues)
* Création d'un module de suivi des abonnements.
* Développement d'un algorithme d'alerte automatique affichant, dès le démarrage de l'application, les abonnements expirant dans moins de 30 jours.

###  Sécurité et Contrôle d'Accès
* **Authentification :** Restriction des fonctionnalités selon le service de l'utilisateur (Administratif, Prêts, Culture).
* **Sécurité de l'API :** Migration des identifiants sensibles vers le fichier `App.config`.
* **Protection Serveur :** Configuration d'un fichier `.htaccess` pour interdire le listage des répertoires sensibles.

###  Amélioration de la Qualité et Déploiement
* Mise en place de tests fonctionnels avec Postman.
* Création d'un installeur Windows (.msi) pour le déploiement client.


## 📸 Aperçu de l'Application


![image](/auth.png)
![image](/expiration.png)
![image](/commandeslivres.png)
![image](/commandesdvd.png)
![image](/revues.png)



# 🕹️ Pac-Man en Python 

Ce projet personnel est un clone du célèbre jeu **Pac-Man**, développé en Python avec la bibliothèque **Pygame**. Le projet est disponible [**ici**](https://github.com/Giovanni2626/pac-man).

## 🚀 Fonctionnalités Clés

*   **Système de Bonus Officiel** : Apparition dynamique des 8 fruits originaux selon le niveau actuel.
    *   *Niv 1* : Cerise | *Niv 2* : Fraise | *Niv 3-4* : Orange | *Niv 5-6* : Pomme
    *   *Niv 7-8* : Melon | *Niv 9-10* : Galboss | *Niv 11-12* : Cloche | *Niv 13+* : Clé
*   **Gestion d'États de Jeu** : Transition fluide entre les modes `READY` (préparation), `PLAY` (en jeu), `PAUSE` et `GAMEOVER`.
*   **Mécaniques Avancées** :
    *   **Intelligence Artificielle** : Les Fantômes poursuivent Pac-Man.
    *   **Système de Power-Up** : Consommation de super-pastilles rendant les fantômes vulnérables.
    *   **Tunnel Loop** : Téléportation fonctionnelle de Pac-Man sur les bords latéraux.
*   **Graphismes Procéduraux** : Tous les sprites (Pac-Man, Fantômes, Fruits) sont dessinés via du code (`pygame.draw`), garantissant un projet léger et performant sans dépendances d'images externes.

## 🛠️ Défis Techniques Résolus

### Collisions
Le plus gros défi a été d'assurer que Pac-Man ne soit pas bloqué par les murs.

### Gestion de la Pause et UX
Intégration d'un système de pause réactif via les touches `ESPACE` ou `P`, permettant de figer l'ensemble de la boucle de jeu (mouvements, timers, animations) sans perdre l'état de la session.

### Déploiement en Exécutable
Le projet est conçu pour être compilé en fichier `.exe` via PyInstaller, rendant l'application installable et jouable sur n'importe quel ordinateur Windows sans installation de Python préalable.

## 📸 Aperçu de l'Application


![image](/pac-man1.png)
![image](/pac-man2.png)
![image](/pac-man3.png)
![image](/pac-man4.png)
![image](/pac-man5.png)

