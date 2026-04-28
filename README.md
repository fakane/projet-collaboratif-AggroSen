# projet-collaboratif-AggroSen# 🌿 AggroSen — L'Agriculture du Sénégal

> La première plateforme de vente d'intrants agricoles en ligne au Sénégal.  
> Qualité, rapidité et confiance depuis 2020.

---

## 📋 Table des matières

- [Présentation](#-présentation)
- [Aperçu du site](#-aperçu-du-site)
- [Structure du projet](#-structure-du-projet)
- [Technologies utilisées](#-technologies-utilisées)
- [Lancer le projet](#-lancer-le-projet)
- [Workflow Git](#-workflow-git)
- [Rôles de l'équipe](#-rôles-de-léquipe)
- [Auteurs](#-auteurs)

---

## 🎯 Présentation

**AggroSen** est un site web statique réalisé dans le cadre d'une simulation de workflow Git/GitHub en conditions réelles d'entreprise. Le projet simule une plateforme e-commerce agricole destinée aux agriculteurs sénégalais, leur permettant de commander en ligne des semences, engrais, matériels d'irrigation, pesticides et bien plus encore.

Ce projet met en pratique :
- La collaboration en équipe via **Git et GitHub** (branches, PR, merge, résolution de conflits)
- Le développement **HTML5 / CSS3** structuré et professionnel
- L'organisation par **rôles** : QA, Chef de Projet, Dev Frontend, Dev Backend

---

## 🖥️ Aperçu du site

Le site comprend les sections suivantes :

| Section | Description |
|---|---|
| **Navbar** | Navigation fixe avec logo, liens et bouton « Commander » |
| **Hero** | Bannière principale avec titre, description et statistiques clés |
| **Catégories** | Grille de 8 catégories (Semences, Engrais, Tracteurs, Irrigation…) |
| **Produits** | Catalogue avec prix FCFA, badges et boutons d'action |
| **Pourquoi Nous** | 6 arguments de confiance (qualité, livraison, paiement flexible…) |
| **Promo Banner** | Offre saisonnière hivernage 2025 (-15% sur les semences) |
| **Témoignages** | Avis clients de Kaolack, Thiès, Saint-Louis |
| **Newsletter** | Formulaire d'abonnement email |
| **Footer** | Liens, contact, réseaux sociaux, mentions légales |

---

## 📁 Structure du projet

```
aggrosen/
├── index.html        # Page principale du site
├── css/
│   └── style.css     # Feuille de styles (variables, responsive, animations)
├── assets/           # Images, icônes et ressources statiques
└── README.md         # Documentation du projet
```

> ⚠️ Le CSS est **séparé** du HTML (`css/style.css`) conformément aux bonnes pratiques de développement web.

---

## 🛠️ Technologies utilisées

- **HTML5** sémantique (`section`, `nav`, `footer`, `header`)
- **CSS3** avec variables custom (`--green`, `--yellow`…), Flexbox, Grid, animations
- **Google Fonts** : [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) (titres) + [DM Sans](https://fonts.google.com/specimen/DM+Sans) (corps)
- **Design Responsive** : adapté mobile, tablette et desktop
- Aucun framework JavaScript — site **100% statique**

---

## 🚀 Lancer le projet

Aucune installation requise. Il suffit d'ouvrir le fichier HTML dans un navigateur :

```bash
# Cloner le dépôt
git clone git@github.com:<org>/aggrosen.git

# Aller dans le dossier
cd aggrosen

# Ouvrir dans le navigateur
open index.html
# ou double-cliquer sur index.html depuis votre explorateur de fichiers
```

> 💡 Pour un meilleur rendu (polices Google Fonts), une connexion internet est recommandée.

---

## 🌿 Workflow Git

Ce projet suit un workflow Git structuré en **7 phases** :

```
Phase 0 → Initialisation (QA crée le repo, pousse sur main, crée dev)
Phase 1 → Clone & Préparation (toute l'équipe clone et se place sur dev)
Phase 2 → Attribution des tâches (Chef de Projet, Trello/Notion)
Phase 3 → Développement (branches feature/, commits atomiques, PR → dev)
Phase 4 → Revue & Tests (QA examine les PR, tests manuels)
Phase 5 → Merge & Conflits (QA merge, développeurs résolvent les conflits)
Phase 6 → Release (PR dev → main, validation CP + QA)
Phase 7 → Démo & Rétrospective
```

### Convention de nommage des branches

```
feature/<role>-<description>

Exemples :
  feature/dev-navbar
  feature/dev-hero-section
  feature/back-assets
  feature/qa-tests-responsive
```

### Règles immuables

- Toute tâche → une branche dédiée
- Les PR ciblent **toujours** la branche `dev`
- **QA** valide et merge les PR
- Les merges vers `main` se font uniquement avec validation **CP + QA**

### Commandes essentielles

```bash
# Cloner le dépôt
git clone https://github.com/fakane/projet-collaboratif-AggroSen.git

# Se placer sur dev
git checkout dev && git pull origin dev

# Créer sa branche de travail
git checkout -b feature/<role>-<tache>

# Commiter son travail
git add . && git commit -m "feat: description claire"

# Pousser et ouvrir une PR
git push -u origin feature/<role>-<tache>

# Synchroniser avec dev (après un merge d'une autre PR)
git checkout dev && git pull origin dev

# Résoudre un conflit
git merge dev
# → résoudre dans l'éditeur
git add . && git commit -m "chore: resolve conflicts"
git push

# Supprimer une branche remote obsolète
git push origin --delete feature/<role>-<tache>
```

---

## 👥 Rôles de l'équipe

| Rôle | Responsabilités |
|---|---|
| **QA (Testeur)** | Création du repo, revue des PR, tests manuels, merge, nettoyage |
| **Chef de Projet** | Planification, attribution des tâches (Trello), documentation, validation finale |
| **Dev Frontend** | HTML/CSS (index.html, style.css), responsive, corrections sur retour QA |
| **Dev Backend** | Architecture, assets, intégration, chemins relatifs, résolution de conflits structurels |

---

## ✅ Checklist avant d'ouvrir une PR

- [ ] Je suis à jour avec `dev` (`git pull origin dev`)
- [ ] Ma branche a un seul objectif clairement défini
- [ ] Mes commits sont clairs et atomiques
- [ ] J'ai ajouté une description à la PR
- [ ] J'ai lié la carte Trello/Notion
- [ ] J'ai testé l'affichage localement (desktop + mobile)

---

## ✅ Checklist QA avant de merger

- [ ] Aucun conflit dans la PR
- [ ] La PR cible bien `dev`
- [ ] Tests manuels OK (desktop & mobile)
- [ ] Aucun asset trop lourd (> 200 Ko sans justification)
- [ ] README mis à jour si nécessaire

---

## ✍️ Auteurs

Projet réalisé dans le cadre d'une **simulation de workflow Git/GitHub en conditions réelles d'entreprise** avec :

PAPA MBACKE NDIAYE : CHEF DE PROJET

FATOU KANE THIAM   : QA

NDEYE MAGUETTE TALL: DEV FRONTEND

MARIETOU SALL      :DEV BACKEND




---

*Conçu avec ❤️ pour les agriculteurs sénégalais*
