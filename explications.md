# Simplification du CSS

Ce document résume simplement les modifications apportées pour nettoyer et optimiser le fichier `framework.css` sans altérer le rendu de la page.

## Ce qui a été modifié

1. **Élimination du surplus dans `:root`**
   - Retrait des variables de tailles, graisses et couleurs non utilisées.
   - Suppression des niveaux d'indirection complexes (ex: `--padding-xs: var(--gap-xs)`). Les valeurs sont désormais directes et lisibles.

2. **Nettoyage des classes inutilisées**
   - Retrait des styles de composants absents du HTML (`.modal`, `.input-control`, `.search-bar`, `.card-grid`).
   - Retrait des colonnes de grille inutiles. Seules `.col-3`, `.col-4` et `.col-6` ont été conservées.

3. **Optimisation des styles de base**
   - Simplification de la typographie globale et des marges des titres (`h1`, `h2`, `h4`, `h5`, `h6`).
   - Retrait des styles génériques trop restrictifs sur `p`, `span`, `div`.

4. **Corrections et intégration**
   - Ajout de la classe `.mb-0 { margin-bottom: 0 !important; }` qui était présente dans le HTML mais manquante dans le CSS.

## Résultat
Le fichier CSS est passé de **667 lignes à 240 lignes** (-64%), le rendant plus rapide à charger et beaucoup plus facile à maintenir.
