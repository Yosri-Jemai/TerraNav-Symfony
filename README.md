# TerraNav - Plateforme Intégrée de Voyage et Transport

## Aperçu 🌍

TerraNav est une plateforme web complète développée dans le cadre du projet d'intégration de 3ème année à **Esprit School of Engineering**. Cette application combine des services de réservation de voyages, d'hébergements et de transports avec une interface utilisateur moderne et intuitive, offrant une expérience utilisateur fluide et responsive.

![Logo TerraNav](public/img/TerraNav.png)

## Fonctionnalités principales ✨

### Gestion des Voyages 🧳
- **Catalogue de voyages** : Exploration et filtrage des voyages par destination, prix et dates
- **Réservation de voyages** : Système complet de réservation avec gestion des places disponibles
- **Offres promotionnelles** : Gestion des réductions et offres spéciales avec notifications
- **Génération IA** : Descriptions de voyages et suggestions d'activités générées par OpenAI
- **Informations météo** : Affichage des prévisions météorologiques des destinations
- **Calendrier d'événements** : Organisation visuelle des voyages à venir
- **Exportation au format ICS** : Ajout des voyages aux calendriers personnels

### Système de Transport 🚗
- **Recherche avancée** : Filtrage par type de transport, capacité et prix
- **Calcul de distance** : Intégration avec Mapbox pour l'estimation des distances
- **Gestion des trajets** : Interface complète pour créer et gérer les trajets
- **Réservation de transports** : Système de réservation avec sélection de dates
- **Exportation PDF** : Génération de documents PDF pour les réservations
- **Géolocalisation** : Suggestion intelligente de lieux en fonction de l'adresse IP

### Gestion des Hébergements 🏨
- **Catalogue d'hébergements** : Recherche par type, ville et disponibilité
- **Gestion des chambres** : Interface détaillée des chambres disponibles
- **Réservation d'hébergement** : Processus simplifié de réservation
- **Import/Export Excel** : Gestion des données via fichiers Excel
- **Conversion de devises** : Affichage des prix dans différentes monnaies
- **Galerie d'images** : Visualisation des hébergements et chambres

### Système de Réservation et Paiement 💳
- **Panier d'achat** : Ajout et gestion de multiples réservations
- **Historique des réservations** : Suivi des réservations passées et futures
- **Codes QR** : Génération de codes QR pour les confirmations de réservation
- **Paiement en ligne** : Intégration avec services de paiement sécurisés
- **Confirmation par email** : Envoi automatique de confirmations

### Fonctionnalités Sociales 💬
- **Publications et commentaires** : Partage d'expériences de voyage
- **Système de likes** : Interaction sociale sur les publications
- **Modération de contenu** : Gestion des publications par les administrateurs
- **Réclamations utilisateurs** : Système de gestion des réclamations

### Sécurité et Authentification 🔒
- **Authentification multi-méthodes** : Email/mot de passe classique et OAuth (Google)
- **Reconnaissance faciale** : Connexion biométrique via microservice dédié
- **Gestion des rôles** : Droits d'accès différenciés pour clients, agences et administrateurs
- **Réinitialisation de mot de passe** : Procédure sécurisée par email

### Administration 👨‍💼
- **Tableau de bord** : Interface d'administration complète
- **Statistiques visuelles** : Graphiques et indicateurs de performance
- **Gestion des utilisateurs** : Administration complète des comptes
- **Rapports exportables** : Génération de rapports aux formats CSV, Excel et PDF

## APIs et Services Intégrés 🔌

### Cartographie et Géolocalisation
- **Mapbox** : Affichage de cartes interactives et géocodage
- **OpenRouter Service** : Calcul d'itinéraires et distances entre points

### IA et Services Cognitifs
- **OpenAI API** : Génération de descriptions et suggestions d'activités
- **Reconnaissance faciale** : Microservice dédié pour l'authentification biométrique

### Services de Voyage
- **Amadeus API** : Recherche de vols et informations aéroportuaires
- **AviationStack** : Données sur les aéroports et compagnies aériennes
- **API Météo** : Prévisions météorologiques des destinations

### Communication
- **Twilio** : Envoi de SMS pour notifications et confirmations
- **Mailer** : Service d'emails pour les confirmations et alertes

### Paiement et Finances
- **API de conversion monétaire** : Conversion dynamique des prix
- **Stripe** : Traitement sécurisé des paiements en ligne

### Utilitaires
- **QR Code Generator** : Création de QR codes pour les réservations
- **PhpSpreadsheet** : Import/export de données en format Excel

## Architecture Technique 🏗️

### Backend
- **Symfony 6.4** : Framework PHP moderne avec architecture MVC
- **Doctrine ORM** : Mapping objet-relationnel pour la gestion de base de données
- **MySQL** : Système de gestion de base de données relationnelle
- **API Platform** : Framework pour création rapide d'API REST

### Frontend
- **Twig** : Moteur de templates pour Symfony
- **Bootstrap 5** : Framework CSS responsive
- **JavaScript** : Interactivité côté client
- **Chart.js** : Bibliothèque de visualisation de données
- **Mapbox GL JS** : SDK JavaScript pour cartes interactives

### Services et utilitaires
- **KnpPaginatorBundle** : Pagination des résultats
- **Symfony Messenger** : Gestion des tâches asynchrones
- **Dompdf** : Génération de documents PDF
- **OAuth** : Authentification via services tiers (Google)
- **Docker** : Conteneurisation du service de reconnaissance faciale

## Structure du projet 🗂️

```
TerraNav/
├── assets/            # Ressources frontend (JS, CSS)
├── config/            # Configuration de l'application et des services
├── facial-auth/       # Microservice Docker de reconnaissance faciale
├── migrations/        # Migrations de base de données
├── public/            # Fichiers publiquement accessibles
├── src/
│   ├── Command/       # Commandes console personnalisées
│   ├── Controller/    # Contrôleurs organisés par domaine fonctionnel
│   │   ├── Admin/     # Contrôleurs d'administration
│   │   ├── hebergements/ # Gestion des hébergements
│   │   ├── reservations/ # Gestion des réservations
│   │   ├── transports/   # Gestion des transports et trajets
│   │   ├── utilisateurs/ # Gestion des utilisateurs
│   │   └── voyages/      # Gestion des voyages et offres
│   ├── Entity/        # Entités Doctrine
│   ├── Form/          # Types de formulaires
│   ├── Repository/    # Repositories par domaine
│   ├── Security/      # Authentification et autorisation
│   ├── Service/       # Services applicatifs
│   └── Validator/     # Contraintes de validation personnalisées
└── templates/         # Templates Twig organisés par fonctionnalité
```

## Installation 🚀

1. Clonez le dépôt :
```bash
git clone https://github.com/votre-utilisateur/TerraNavSymfony.git
```

2. Installez les dépendances :
```bash
composer install
npm install
```

3. Configurez votre fichier .env avec :
   - Paramètres de base de données
   - Clés API (Mapbox, OpenAI, Amadeus, Twilio)
   - Configuration email
   - Paramètres OAuth

4. Créez la base de données et exécutez les migrations :
```bash
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
```

5. Compilez les assets :
```bash
npm run build
```

6. Lancez le serveur de développement :
```bash
symfony serve
```

7. Pour la reconnaissance faciale :
```bash
docker-compose up -d facial-auth
```

## Démarrage rapide 🏃‍♂️

Après installation, accédez à `http://127.0.0.1:8000` dans votre navigateur.

Utilisez les comptes de démonstration :
- **Client** : client@terranav.com / password
- **Agence de voyage** : voyage@terranav.com / password
- **Agence de transport** : transport@terranav.com / password
- **Administrateur** : admin@terranav.com / password

## API Endpoints 📡

### API Voyages
- `GET /api/voyages` : Liste des voyages disponibles
- `GET /api/voyages/{id}` : Détails d'un voyage
- `GET /api/voyages-expires` : Liste des voyages expirés

### API Transports
- `POST /check-distance` : Calcul de distance entre deux points
- `GET /cities/autocomplete` : Suggestions de villes pour l'autocomplétion

### API Réservations
- `GET /api/calendar/events` : Events pour le calendrier de réservations
- `POST /transport/reserve` : Réservation d'un transport

### API Hébergements
- `GET /hebergements` : Liste des hébergements disponibles
- `POST /currency/change` : Changement de devise d'affichage

## Captures d'écran 📸

<div align="center">
  <img src="public/img/screenshots/home.jpg" width="45%" alt="Page d'accueil"/>
  <img src="public/img/screenshots/transport.jpg" width="45%" alt="Recherche de transport"/>
  <img src="public/img/screenshots/voyage.jpg" width="45%" alt="Détails d'un voyage"/>
  <img src="public/img/screenshots/dashboard.jpg" width="45%" alt="Tableau de bord"/>
</div>

## Équipe de développement 👥

Ce projet a été réalisé par une équipe d'étudiants de l'**Esprit School of Engineering** dans le cadre du projet d'intégration PIDEV 3A.

## Contribution 🤝

Nous accueillons les contributions à ce projet :

1. Fork du dépôt
2. Création d'une branche (`git checkout -b feature/amelioration`)
3. Commit des changements (`git commit -m 'Ajout d'une nouvelle fonctionnalité'`)
4. Push vers la branche (`git push origin feature/amelioration`)
5. Ouverture d'une Pull Request

## Remerciements 🙏

Nous remercions:
- Nos encadrants à l'**Esprit School of Engineering**
- Les équipes de documentation des APIs utilisées
- La communauté Symfony pour leurs ressources et supports

---

© 2025 TerraNav | Développé avec 💙 par les étudiants de l'**Esprit School of Engineering**
