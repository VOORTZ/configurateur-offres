# Configurateur Offres

Prototype front-end (fichier unique `index.html`) pour orienter rapidement un client vers une recommandation Internet / Mobile / Options.

## Utilisation locale

```bash
python3 -m http.server 4173
```
Puis ouvrez `http://localhost:4173`.

## Flux GitHub recommandé

1. Travailler sur une branche (ex: `work`).
2. Ouvrir une Pull Request vers `main`.
3. Résoudre les conflits éventuels puis **merge** la PR.
4. Rafraîchir `main` pour voir la version à jour.

> Les changements ne s'affichent pas sur `main` tant que la PR n'est pas fusionnée.

## Notes UX implémentées

- Parcours question par question (tablette-friendly).
- Validation minimale avant passage à la question suivante.
- Barre de progression alignée sur le nombre réel de questions.
- Restauration d'état robuste (URL + localStorage) avec normalisation.
