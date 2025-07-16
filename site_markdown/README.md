# 📚 Template CERTA - Guide de création de supports de formation

Ce repository contient un template complet pour créer des supports de formation CERTA avec Jekyll et GitHub Pages.

## 🎯 Objectif

Créer rapidement des sites web de formation professionnels avec :
- Style CERTA uniforme
- Navigation intuitive
- Déploiement automatique sur GitHub Pages
- Support vidéo et multimédia

## 🚀 Démarrage rapide

### 1. Créer un nouveau repository

```bash
# Cloner ce template
git clone https://github.com/taccary/codespaces-CERTA.git nom-de-votre-formation
cd nom-de-votre-formation

# Nettoyer l'historique git
rm -rf .git
git init
git add .
git commit -m "Initial commit - Template CERTA"
```

### 2. Configuration de base

#### A. Modifier `_config.yml`
```yaml
title: "Votre titre de formation"
description: "Description de votre formation"
baseurl: "/nom-de-votre-repo" # Nom de votre repository GitHub
url: "https://votre-username.github.io"

# Métadonnées CERTA
author:
  name: "Votre Nom"
  email: "votre.email@ac-academie.fr"

# Thème et plugins (ne pas modifier)
theme: minima
plugins:
  - jekyll-feed
  - jekyll-sitemap
  - jekyll-seo-tag

# Configuration Kramdown (ne pas modifier)
markdown: kramdown
kramdown:
  input: GFM
  syntax_highlighter: rouge
  hard_wrap: false
```

#### B. Personnaliser `index.md`
Modifiez les métadonnées YAML en en-tête :
```yaml
---
title: "Votre formation - réseau CERTA 2025"
subtitle: "Sommaire"
authors: 
  - "Votre Nom"
date: 2025-MM-DD
description: "Description de votre formation"
tags: 
  - "CERTA"
  - "Votre sujet"
---
```

### 3. Structure des fichiers

```
votre-formation/
├── _config.yml              # Configuration Jekyll
├── _layouts/
│   └── default.html         # Layout principal avec style CERTA
├── assets/
│   └── css/
│       └── style.css        # Styles CERTA personnalisés
├── index.md                 # Page d'accueil
├── intro.md                 # Introduction
├── webinaire.md            # Page vidéo/webinaire
├── ressources.md           # Ressources et templates
├── Gemfile                 # Dépendances Ruby
└── README.md               # Ce fichier
```

## 🎨 Utilisation du style CERTA

### Couleurs disponibles
- **Rouge CERTA** : `#8C104F`
- **Bleu CERTA** : `#193B70`
- **Gris clair** : `#f8f9fa`

### Classes CSS personnalisées

#### Centrage de contenu
```markdown
**[Texte centré]**
{: .text-center}
```

#### Boutons de navigation
```markdown
**[← Précédent](page-precedente.md)** | **[Suivant →](page-suivante.md)**
{: .navigation-buttons}
```

#### Boîtes d'information
```markdown
> 💡 **Astuce :** Votre conseil utile
{: .info-box}
```

#### Mise en évidence
```markdown
**Texte important**
{: .highlight}
```

### Intégration de vidéos

#### Vidéo YouTube
```markdown
<div class="video-container">
  <iframe src="https://www.youtube.com/embed/VIDEO_ID" 
          frameborder="0" 
          allowfullscreen>
  </iframe>
</div>
```

#### Badge vidéo avec lien
```markdown
[![Voir le webinaire](https://img.shields.io/badge/📹_Voir_le_webinaire-YouTube-red?style=for-the-badge)](https://youtube.com/watch?v=VIDEO_ID)
{: .text-center}
```

## 🛠️ Développement local

### Prérequis
- Ruby (installé automatiquement dans Codespaces)

### Installation et test

```bash
# Dans votre Codespace ou environnement local
cd votre-formation

# Installer les dépendances
gem install bundler jekyll
bundle install --path vendor/bundle

# Démarrer le serveur de développement
bundle exec jekyll serve --host 0.0.0.0 --port 4000

# Ouvrir dans le navigateur
# http://localhost:4000
```

### Workflow de développement

1. **Modifier vos fichiers** `.md`
2. **Vérifier en local** avec `bundle exec jekyll serve`
3. **Commiter et pusher** vers GitHub
4. **GitHub Pages** se charge automatiquement du déploiement

## 📦 Déploiement sur GitHub Pages

### Configuration automatique

1. **Pousser votre code** vers GitHub
2. **Aller dans Settings > Pages**
3. **Source** : Deploy from a branch
4. **Branch** : main / (root)
5. **Sauvegarder**

Votre site sera disponible à : `https://votre-username.github.io/nom-de-votre-repo`

### Vérification du déploiement

- **Actions** : Vérifiez que le build Jekyll réussit
- **Environments** : Consultez l'URL de déploiement
- **En cas d'erreur** : Vérifiez les logs dans Actions

## 📝 Création de contenu

### Métadonnées YAML

Chaque fichier `.md` doit commencer par :

```yaml
---
title: "Titre de la page"
subtitle: "Sous-titre optionnel"
authors: 
  - "Votre Nom"
date: 2025-MM-DD
description: "Description pour le SEO"
tags: 
  - "CERTA"
  - "Tag1"
  - "Tag2"
---
```

### Navigation entre pages

```markdown
**[← Page précédente](precedente.md)** | **[Page suivante →](suivante.md)**
{: .navigation-buttons}
```

### Tableaux

```markdown
| Colonne 1 | Colonne 2 | Colonne 3 |
|-----------|-----------|-----------|
| Donnée 1  | Donnée 2  | Donnée 3  |
| Donnée 4  | Donnée 5  | Donnée 6  |
{: .table-certa}
```

## 🔧 Personnalisation avancée

### Modifier les couleurs CERTA

Éditez `assets/css/style.css` :

```css
:root {
  --certa-red: #8C104F;
  --certa-blue: #193B70;
  --certa-light: #f8f9fa;
}
```

### Ajouter des styles personnalisés

```css
/* Votre style personnalisé */
.ma-classe-custom {
  background-color: var(--certa-red);
  color: white;
  padding: 1rem;
  border-radius: 8px;
}
```

## 📋 Checklist de création

- [ ] Repository créé et cloné
- [ ] `_config.yml` personnalisé
- [ ] `index.md` modifié avec vos informations
- [ ] Pages de contenu créées
- [ ] Navigation ajoutée entre les pages
- [ ] Test en local réussi
- [ ] GitHub Pages configuré
- [ ] Déploiement vérifié

## 🆘 Résolution de problèmes

### Erreur de build Jekyll

```bash
# Vérifier les erreurs localement
bundle exec jekyll build --verbose

# Problèmes fréquents :
# - Dates mal formatées : utilisez 2025-06-30
# - YAML mal formé : vérifiez l'indentation
# - Liens cassés : vérifiez les chemins
```

### Styles qui ne s'appliquent pas

1. Vérifiez que `style.css` est dans `assets/css/`
2. Contrôlez le `baseurl` dans `_config.yml`
3. Testez en local avant de déployer

### Pages qui ne s'affichent pas

1. Vérifiez les métadonnées YAML
2. Contrôlez les noms de fichiers (pas d'espaces)
3. Assurez-vous que les liens sont corrects

## 📞 Support

Pour toute question sur ce template :
- **Documentation Jekyll** : https://jekyllrb.com/docs/
- **GitHub Pages** : https://docs.github.com/pages/
- **Markdown** : https://guides.github.com/features/mastering-markdown/

---

**Template créé par le réseau CERTA - 2025**
{: .text-center}

*Bon développement de vos supports de formation !* 🚀
{: .text-center}
