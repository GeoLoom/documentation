# 🌊 Gitflow - Workflow de développement

## Branches principales
- `main` : dernière version en production
- `develop` : version stable pour développement

## Branches secondaires
- `feature/*` : nouvelles fonctionnalités
- `Bugfix/*` : corrections mineures
- `release/*` : version prête pour la prod
- `hotfix/*` : correction urgente sur la prod

## Règles de contribution
- Pas de push direct sur `main` ni `develop`
- Crée une PR pour chaque `feature/` ou `fix/`
- Ajoute un titre clair et une description


## Command
- ``git flow feature start login-page``
- Crée une branche `feature/login-page` depuis `develop`.
- ``git flow feature finish login-page``
- Merge dans `develop` et supprime la branche locale.
- ``git flow release start 1.0.0``
- Crée `release/1.0.0` depuis `develop`.
- ``git flow release finish 1.0.0``
- Merge dans `main` + `develop` + crée un tag v1.0.0
- ``git flow hotfix start urgent-fix``
- Depuis `main`
- ``git flow hotfix finish urgent-fix``
- Merge dans `main` + `develop` + tag version
