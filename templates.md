---
title: "Utiliser et créer des Template Codespace"
subtitle: "GitHub Education : Templates"
authors: 
  - "Tiphaine Accary-Barbier"
  - "Maëlle Taurand"
date: 2025-06-30
description: "Collection de templates GitHub Codespaces pour l'enseignement : exemples pratiques et configurations prêtes à l'emploi"
tags: 
  - "GitHub Codespaces"
  - "Templates"
  - "Éducation"
  - "SIO"
  - "Développement"
license: "GNU GPL v3"
language: "fr"
---

# GitHub Education : Utiliser et créer des Template Codespace


## Table des matières

- [Introduction aux Templates GitHub Codespaces](#introduction-aux-templates-github-codespaces)
- [Exemples de Templates \"maison\" utilisés en TP et AP SIO](#exemples-de-templates-utilisés-en-tp-et-ap-sio)

## Introduction aux Templates GitHub Codespaces

Dans nos pratiques pédagogiques, la configuration des environnements de
développement peut représenter un frein, tant pour nous que pour nos
étudiants. **GitHub Codespaces**, et plus particulièrement
ses **templates**, offrent une solution moderne et efficace à ce
problème.

Un *template Codespace* est un modèle d'environnement de développement
prêt à l'emploi, hébergé dans le cloud, et directement lié à un dépôt
GitHub. Il permet de standardiser les outils, les dépendances et les
configurations nécessaires à un projet, tout en supprimant les problèmes
liés aux différences de machines ou de systèmes d'exploitation.

Pour nous, enseignants, cela signifie :

-   Un **gain de temps considérable** lors de la préparation des TP ou
    projets.

-   Une **expérience homogène** pour tous les étudiants, quel que soit
    leur matériel.

-   Une **réduction des problèmes techniques** en début de séance.

-   Une **meilleure reproductibilité** des travaux pratiques d'une année
    sur l'autre.

Vous pouvez créer exactement le Template qui vous convient en écrivant
dans votre dépôt un DockerFile adapté mais vous pouvez également
utiliser un modèle \"officiel\" GitHub
<https://github.com/codespaces/templates>

Vous pouvez bien sur faire un mix des 2 en partant d'un modèle et en
personnalisant ses paramètres dans un *DockerFile* et/ou dans le fichier
*.devcontainer/devcontainer.json*.

<u>Ressource</u> :
<https://docs.github.com/fr/codespaces/developing-in-a-codespace/creating-a-codespace-from-a-template>

## Exemples de Templates utilisés en TP et AP SIO

Voici des exemples de dépôts (créés et/ou utilisés avec mes étudiants de
SIO) qui sont configurés pour fonctionner dans des Codespaces. Ces
dépôts ont le statut de Template pour pouvoir ensuite être utilisés
comme modèle dans les devoirs Classroom. Je leur ai donné une visibilité
publique pour pouvoir vous les partager.

Ils sont **sous licence GNU3** et donc librement partageable. Cependant,
ils sont amenés à évoluer dans le temps (correction de bug, mise à jour
de composants, \...) donc, si après les avoir testés, vous voulez les
utiliser de votre coté en les adaptant, **je vous conseille d'en faire
des forks**.

Le choix de ces dépôts et de vous montrer des exemples qui mettent en
œuvre différentes technologies et sur différents niveaux. Concrètement
au lycée on en utilise en B1, B2 SLAM, B3 SLAM et AP.

Les 5 premiers exemples sont des templates \"maison\", bricolés pour
répondre à mes besoins. Les 2 derniers sont des exemples de dépôts
publics directement exécutables dans un Codespace de base sans config
spécifique :

### Templates "maison"

| **Techno** | **Utilisation** | **Lien et explications** |
|------------|-----------------|---------------------------|
| **HTML/CSS/JS** | SIO1 sem1 B1 | [HTML-decouverte](https://github.com/icof/HTML-decouverte)<br>Utilisation du template Codespace de base pour les TP de HTML/CSS/JS. Pas de Dockerfile, installation du serveur http avec npm (préinstallé). |
| **PHP MVC** | SIO1-SLAM sem2 AP | [AP-SIO1-SLAM-oceane-MVC](https://github.com/icof/AP-SIO1-SLAM-oceane-MVC)<br>Codespace LAMP PHP avec Xdebug depuis une image spécifique avec un Dockerfile complexe et des scripts Bash + phpUnit + phpDocumentor |
| **Java** | SIO1-SLAM sem2 révisions d'été POO | [revisions-POO-Java](https://github.com/taccary/revisions-POO-Java)<br>Codespace Java (Maven avec JUnit) pour les travaux d'été de révision. Il contient un TP de révisions créé par Hervé L'Helguen |
| **PHP API Laravel** | SIO2-SLAM Sem3 - B2 | [API-laravel-Oceane](https://github.com/taccary/API-laravel-Oceane)<br>POC d'API Laravel avec sécurisation JWT et documentation Swagger. |
| **React Native** | SIO2-SLAM Sem3 B2 (futurs TP) | [reactNative-oceane](https://github.com/taccary/reactNative-oceane)<br>3 Applications React Native : Une multi-onglets et 2 interagissant avec une API (démarrée depuis le codespace API Laravel), avec une partie CRUD protégé par authentification JWT<br>Consultable en émulation web et sur mobile via Expo |

### Dépôts publics executables directement dans un Codespace sans configuration

| **Techno** | **Utilisation** | **Lien et explications** |
|------------|-----------------|---------------------------|
| **Python** | SIO1 | Python est installé dans le Codespace de base. On trouve sur github des dépôts publics vous permettant de tester très rapidement, par exemple :<br>[python-exercices](https://github.com/hamzaezzine/python-exercices)<br>Il vous suffit d'ouvrir ce dépôt dans un codespace puis d'exécuter les exercices avec la commande "python exoxxx.py". |
| **JavaScript** | SIO1 sem1 B1 | Node est installé dans le Codespace de base. Voici un exemple de dépôt public "Dojo d'exercices de code en javascript vérifiés par des tests unitaires (plateforme d'apprentissage)" partagé par javascriptdezero<br>[coding-dojo](https://github.com/javascriptdezero/coding-dojo/tree/master)<br>Il est possible d'exécuter un codespace directement sur le dépôt public ou de faire un fork du projet. Le dojo est prêt à l'emploi ! |

## Dépots "vierges" et consignes pour démarrer un projet avec un Codespace


**[← Webinaire](webinaire.md)** | **[Retour au sommaire](README.md)** | **[??? →](à venir)**