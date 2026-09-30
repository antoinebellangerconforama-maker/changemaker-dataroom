# Data room · Groupe 13 (ChangeMaker Project 2026)

Site statique publié sur GitHub Pages.

- `index.html` : le design et l'affichage (ne change quasiment jamais)
- `data.json` : tout le contenu (onglets, sections, documents, mot d'accueil, jalons)
- Source des documents : le dossier Google Drive de l'équipe (partagé en lecture « tous les utilisateurs disposant du lien »)

## Mettre à jour

1. Demander la modification à Claude (ex. « ajoute un onglet Finance », « passe le PESTEL en V3 », « resynchronise avec le Drive »).
2. Claude modifie `data.json` dans ce dossier.
3. GitHub Desktop : **Commit to main** puis **Push origin**. Le site est à jour en 1 minute environ.

## Format d'un document dans data.json

```json
{ "title": "PESTEL", "kind": "pdf", "driveId": "ID_DRIVE", "status": "final",
  "version": "V2", "date": "2026-09-30", "owner": "email@gmail.com", "note": "Une ligne de description" }
```

- `kind` : pdf, doc, sheet, slides, pptx, csv, ou link (avec `url` à la place de `driveId`)
- `status` : final, working (en cours), todo (à venir, avec `due`), archived

## Tester en local

`python3 -m http.server` dans ce dossier, puis ouvrir http://localhost:8000
