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

## Lisibilité mode client

En mode client, l'interface est volontairement simplifiée :
- feedback court,
- moins de détails techniques visibles,
- résultat final synthétique (offre recommandée + mobile recommandé).

## Référentiel prix Orange.fr (mise à jour)

Tarifs vérifiés depuis les pages Orange.fr/Boutique Orange lors de la dernière mise à jour du code :
- Internet fibre: Série Spéciale Livebox Lite 29,99€ ; Livebox Fibre 29,99€ puis 42,99€ ; Livebox Up Fibre 39,99€ puis 51,99€ ; Livebox Max Fibre 47,99€ puis 57,99€.
- Mobile premium (hors remises): Forfait 200Go 5G = 47,99€ ; Forfait 300Go 5G = 67,99€ ; Forfait 500Go 5G+ = 84,99€.
- Remises appliquées dans le configurateur: Open/internet de 8€ (200Go) et 15€ (300/500Go).

## Stratégie d'affichage prix

Le configurateur affiche désormais en priorité le **prix mensuel de référence** (et non le prix promo des 12 premiers mois),
afin de garder une marge commerciale pour proposer d'autres options en boutique (ex: Maison Protégée).
Quand une remise pack est active, l'UI affiche le **prix avant remise** puis le **prix remisé** pour valoriser l'avantage client.

## Sélection mobile client (Orange.fr)

Le parcours mobile propose désormais une sélection de smartphones avec prix issus de la boutique Orange,
avec un parcours en 2 clics :
- choix de la **marque**,
- puis choix du **modèle**.

Pendant la sélection, les prix des mobiles ne sont pas affichés pour garder le focus besoin.
Le prix est affiché au récapitulatif final, en lien avec l'offre/forfait proposé.
Le paiement en 24x n'est pas affiché pour le moment : affichage en prix comptant uniquement.

## Budget total affiché

Le résultat affiche un budget total estimé de l'offre complète :
- Internet,
- forfait mobile,
- options sélectionnées.

Le montant est affiché en **€/jour** (base 31 jours) puis en **€/mois**.

## Ajustements UX (lisibilité client)

- Le résultat client est volontairement court : budget total, Internet recommandé, mobile recommandé.
- Le **prix / jour** est mis en avant en premier, avec le rappel **/ mois** juste en dessous.
- Le total peut être affiché **avec** ou **sans options** (bouton de bascule dans le récap).
- La mise en page utilise toute la largeur disponible pour un meilleur confort sur tablette et PC.
