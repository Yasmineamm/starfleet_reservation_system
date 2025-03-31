# Projet StarFleet Reservation System

## Description

Le **StarFleet Reservation System** est un système de gestion de réservations pour une flotte de vaisseaux spatiaux. Ce projet permet aux utilisateurs de gérer les vaisseaux, les missions, les personnes (officiers et civils), et les réservations pour des missions spatiales. Le système permet également de sauvegarder et charger les données dans des fichiers pour garantir la persistance de l'information.

## Fonctionnalités Implémentées

### 1. **Gestion des Vaisseaux**
   - Ajouter, modifier, supprimer et afficher des vaisseaux.
   - Chaque vaisseau peut avoir un nom, un numéro d'immatriculation, et une capacité maximale d'équipage et de passagers.
   - Les vaisseaux sont associés à des missions.

### 2. **Gestion des Personnes**
   - Ajouter des membres d'équipage (officiers) et des civils.
   - Les officiers peuvent être associés à un rôle spécifique (Capitaine, Commander, etc.) et à une spécialité (Commandement, Stratégie, etc.).
   - Les civils ont une destination et un objectif (Tourisme, Recherche, etc.).
   - Afficher la liste des personnes, modifier une personne (nom, prénom, etc.), et supprimer une personne.
   
### 3. **Gestion des Missions**
   - Créer, modifier, annuler et afficher des missions spatiales.
   - Chaque mission peut être associée à un vaisseau spécifique et avoir une destination (Vulcain, Terre, Risa, etc.).
   - Les missions ont des dates de départ et de retour.

### 4. **Gestion des Réservations**
   - Créer une réservation pour une personne pour une mission donnée.
   - Confirmer ou annuler des réservations.
   - Afficher les réservations effectuées pour une mission spécifique ou pour une personne.

### 5. **Recherches**
   - Rechercher des missions par destination, dates, ou places disponibles.
   - Rechercher des personnes par nom ou identifiant.
   - Rechercher des vaisseaux par nom ou immatriculation.

### 6. **Sauvegarde et Chargement des Données**
   - Sauvegarder toutes les données du système dans un fichier à l'aide de la sérialisation.
   - Charger les données à partir d'un fichier sauvegardé pour restaurer l'état du système à son dernier état sauvegardé.

---

## Structure du Projet

Le projet est organisé en plusieurs packages, chacun étant responsable d'une partie spécifique de la gestion du système de réservation.

src/ ├── main/ │ ├── java/ │ │ └── fr/ │ │ └── starfleet/ │ │ ├── modele/ │ │ │ ├── mission/ # Gestion des missions │ │ │ ├── personne/ # Gestion des personnes (officiers et civils) │ │ │ ├── reservation/ # Gestion des réservations │ │ │ └── vaisseau/ # Gestion des vaisseaux │ │ ├── systeme/ # Gestion globale du système de réservation │ │ ├── util/ # Utilitaires (sérialisation, gestion des dates, etc.) │ │ └── Main.java # Point d'entrée principal pour démarrer le programme


- **Modele** : Contient toutes les classes représentant les entités du système (Vaisseau, Mission, Personne, etc.).
- **Systeme** : Contient la classe principale `SystemeReservation` qui gère toutes les opérations du système (ajouter des vaisseaux, des personnes, etc.).
- **Util** : Contient les classes utilitaires pour la sérialisation des données (`FileUtil`), la gestion des dates (`DateUtil`), etc.
