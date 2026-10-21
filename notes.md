# Cours de Git

## Plan de cours
1. Culture G
2. Utiliser un ordinateur sans souris
3. Setup git local et compte GitHub
5. Origin
6. Organisation de travail

2 Notes = CheatSheet commandes Git (Markdown) + Interro écrite (juste les notes)

## Histoire de Git

- Linus Torvalds a créé Git en 2005 pour gérer le développement du noyau Linux.
- BitKeeper était le système de gestion de versions utilisé auparavant, mais il avait des limitations qui ont conduit à la création de Git.
- Puis un jour, Linus a décidé de créer un système de gestion de versions distribué qui serait rapide, efficace et capable de gérer de grands projets avec de nombreux contributeurs.

- Git compare ligne par ligne les fichiers et ne stocke que les différences, ce qui le rend très efficace en termes de stockage et de vitesse.

### Pourquoi apprendre à utiliser Git ?

- Comment faire sans ?
- De très loin le plus utilisé
- Open source
- Travailler seul et en groupe

### Les commandes de git

**La doc officiell** : [https://git-scm.com/book/fr/v2](https://git-scm.com/book/fr/v2)
**Les branches** : [https://learngitbranching.js.org](https://learngitbranching.js.org)

### Les commandes de base

| Commande | Description |
|---|---|
| `git config` | Configure les paramètres de Git (nom d'utilisateur, email, etc.) |
| `git init` | Initialise un dépôt Git dans le répertoire courant |
| `git clone <url>` | Clone un dépôt distant dans le répertoire courant |
| `git status` | Affiche l'état du dépôt (fichiers modifiés, ajoutés, supprimés, etc.) |
| `git diff` | Affiche les différences entre les fichiers modifiés et la dernière version commitée |
| `git log` | Affiche l'historique des commits |
| `git add <fichier>` | Ajoute un fichier à l'index pour le prochain commit |
| `git commit -m "<message>"` | Crée un commit avec le message spécifié |

### Les commandes avancées

| Commande | Description |
|---|---|
| `git rm <fichier>` | Supprime un fichier du dépôt et de l'index |
| `git stash` | Met de côté les modifications en cours pour revenir à un état propre du dépôt |
| `git reset` | Annule les modifications dans l'index et/ou le répertoire de travail |
| `git revert <commit>` | Crée un nouveau commit qui annule les modifications d'un commit précédent |
| `git fetch` | Récupère les modifications depuis le dépôt distant sans les fusionner |

### commande pour bosser en groupe

| Commande | Description |
|---|---|
| `git pull` | Récupère les modifications depuis le dépôt distant et les fusionne avec la branche courante |
| `git push` | Envoie les modifications locales vers le dépôt distant |
| `git branch` | Liste les branches locales et permet de créer, supprimer ou renommer des branches |
| `git switch <branche>` | Change de branche ou restaure des fichiers à partir d'une branche spécifique |
| `git merge <branche>` | Fusionne une branche spécifique dans la branche courante |
| `git rebase <branche>` | Applique les commits de la branche courante sur une autre branche, réécrivant l'historique des commits
### Gitmoji

| Emoji | code | Description |
|---|---|---|
| ✨ | `:sparkles:` | Ajout d'une nouvelle fonctionnalité |
| 🐛 | `:bug:` | Correction d'un bug |
| 📝 | `:memo:` | Ajout ou modification de documentation |
| 🚀 | `:rocket:` | Amélioration des performances |
| 🧪 | `:test_tube:` | Ajout ou modification de tests |
| 🧹 | `:broom:` | Nettoyage du code |
| 📦 | `:package:` | Ajout d'une dépendance |
| 📉 | `:chart_with_downwards_trend:` | Réduction de la taille du code |
| 📈 | `:chart_with_upwards_trend:` | Augmentation de la taille du code |
| 🎨 | `:art:` | Amélioration de l'architecture ou du design |
| 🔧 | `:wrench:` | Modification de la configuration |
| 💡 | `:bulb:` | Ajout d'une idée ou d'une amélioration |
| 🕒 | `:clock12:` | Correction d'un problème de synchronisation |
| 🔒 | `:lock:` | Amélioration de la sécurité |
| 🔍 | `:mag:` | Amélioration de la recherche ou du filtrage |
| 📊 | `:bar_chart:` | Ajout ou modification de statistiques |
| 📅 | `:calendar:` | Ajout ou modification d'un calendrier |

### Faire une clé ssh pour GitHub (sur Mac)

1. Générer une clé SSH : `ssh-keygen -t ed25519 -C "your_email@example.com"`
2. Ajouter la clé SSH à l'agent SSH : `eval "$(ssh-agent -s)"` puis `ssh-add ~/.ssh/id_ed25519`
3. Copier la clé publique : `pbcopy < ~/.ssh/id_ed25519.pub` (ou `cat ~/.ssh/id_ed25519.pub` pour l'afficher dans le terminal)
4. Ajouter la clé publique à votre compte GitHub : Allez dans "Settings" > "SSH and GPG keys" > "New SSH key" et collez la clé publique.