# Livrables

> Tous les documents produits pour mes projets : cadrage, conception, livraisons, administratif.
> Le **code source** des applications vit dans son propre dépôt Git, pas ici.

## Organisation

```
livrables/
├── lahnel/            # Projets de l'ESN LAHNEL
│   └── moovi/
├── freelance/         # Un dossier par client / projet
│   ├── _modele-projet/        # À copier pour chaque nouveau projet
│   ├── erp-dolibarr-agro/
│   ├── paiement-salaires/
│   └── ecommerce-cosmetiques/
├── mba/
│   └── memoire/       # sources/, redaction/, versions-rendues/
└── certifications/
    ├── ai-103/
    └── ai-901/
```

Les projets employeur sont confidentiels et ne sont pas stockés ici.

## Les 4 phases d'un projet

| Dossier | Contenu |
|---------|---------|
| `01-cadrage/` | Cahier des charges, comptes rendus de réunion, devis, besoins client |
| `02-conception/` | Architecture (C4, 4+1), maquettes, modèle de données, spécifications |
| `03-livraisons/` | Versions livrées, PV de recette, manuels utilisateur, formations |
| `04-admin/` | Contrat, bons de commande, factures, échanges contractuels |

## Nouveau projet freelance

```bash
cp -r livrables/freelance/_modele-projet livrables/freelance/<nom-client-projet>
```

## Conventions de nommage

- Dossiers en minuscules, mots séparés par des tirets : `erp-dolibarr-agro`
- Fichiers datés au format `AAAA-MM-JJ_` en préfixe : `2026-10-04_cahier-des-charges_v1.pdf`
- Versions en suffixe : `_v1`, `_v2`, `_final`
- Jamais de mot de passe ni de clé API dans un livrable : utiliser `secrets/` ou `.env`
