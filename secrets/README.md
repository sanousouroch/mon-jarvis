# Secrets

> Ce dossier est **ignoré par Git** (sauf ce README). Rien de ce qui est déposé ici ne sera versionné.

## Où mettre quoi

| Type de secret | Emplacement |
|----------------|-------------|
| Clés API et variables simples (Azure, OpenAI, GitHub...) | `.env` à la racine du workspace |
| Fichiers de clés (JSON de compte de service, certificats `.pem`, `.pfx`, clés SSH) | `secrets/` |
| Accès clients (identifiants ERP, serveurs, hébergeurs) | Gestionnaire de mots de passe (Bitwarden, 1Password, KeePass) |

## Règles

1. **Jamais de secret en clair** dans le code, un livrable, CLAUDE.md ou les fichiers de `context/`.
2. Le fichier `.env.example` (versionné) liste les noms des variables **sans leurs valeurs**. Pour démarrer : `cp .env.example .env`, puis remplir `.env`.
3. Une clé partagée par erreur (commit, capture d'écran, message) doit être **révoquée et régénérée** immédiatement. La supprimer du fichier ne suffit pas : elle reste dans l'historique Git.
4. Une clé par usage et par projet client quand c'est possible, pour pouvoir en révoquer une sans tout casser.
5. Dans chaque dépôt de code client, appliquer la même règle : `.env` ignoré, `.env.example` versionné.
