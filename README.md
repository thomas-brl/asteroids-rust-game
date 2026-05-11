# Jeu Asteroids

## Description

Ce projet est une recréation du jeu **Asteroids**, développée en **Rust** à l’aide de la bibliothèque graphique **Macroquad**.

Le joueur contrôle un vaisseau spatial aux côtés d’astéroïdes qu’il doit éviter ou détruire à l’aide de missiles.

---

## Fonctionnalités du jeu

Il y a 3 types d'objets :
- Astéroïdes
- Vaisseau
- Missiles

Tous sont considérés comme des formes circulaires afin de simplifier la gestion des collisions.

Lorsque le vaisseau ou un astéroïde sort de l'écran, il réapparait du côté opposé

La partie se termine lorsque :
- le vaisseau est détruit
- tous les astéroïdes sont détruits
- le joueur appuie sur `Échap`

### Astéroïdes
- Déplacement à vitesse constante et aléatoire
- Trois tailles possibles : grande, moyenne, petite
- Division en deux astéroïdes plus petits lors des collisions
- Destruction complète lorsqu’ils sont trop petits

### Vaisseau
- Déplacement contrôlé par les flèches du clavier
- Système de vies
- Perte de vie ou destruction lors d’une collision avec un astéroïde

### Missiles
- Déplacement en ligne droite selon l’orientation du vaisseau
- Disparition lors d’une collision ou en sortie d’écran
- Destruction ou fragmentation des astéroïdes

---

## Contrôles

- ⬆ : Avancer
- ⬇ : Reculer
- ⬅ : Rotation gauche
- ➡ : Rotation droite
- `Espace` : Tirer un missile
- `Échap` : Quitter la partie

---

## Architecture du projet

Le projet est structuré en plusieurs modules :

- `asteroid` : gestion des astéroïdes
- `spaceship` : gestion du vaisseau
- `missile` : gestion des projectiles
- `stellarobject` : définition d’un trait commun pour factoriser les comportements des objets du jeu
