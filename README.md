# Configurateur Offres

Outil tablette pour conseiller en boutique Orange.

## Lancer en local

```bash
python3 -m http.server 4173
```

Puis ouvrir `http://localhost:4173`.

## IA live (version actuelle)

Le projet inclut une **IA live locale** (heuristique) qui affiche en temps réel :
- besoins exprimés,
- besoins non exprimés probables,
- questions à poser au client,
- potentiel premium sur le mobile.

## Logique mobile premium

Le parcours mobile intègre désormais :
- un indicateur "projet d'achat mobile",
- une recommandation prioritaire vers les forfaits **200/300/500 Go** selon le profil et les signaux IA,
- un rappel des avantages liés au mobile pour aider l'argumentaire vendeur.
