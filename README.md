# GanttFlow Pro

**Application de planification Gantt professionnelle — mono-fichier HTML, sans dépendance, 100% hors-ligne.**

![GanttFlow Pro](https://img.shields.io/badge/version-1.0-blue) ![HTML](https://img.shields.io/badge/HTML-single%20file-orange) ![License](https://img.shields.io/badge/license-MIT-green)

---

## Fonctionnalités

### Planning
- Diagramme de Gantt interactif avec zoom Jours / Semaines / Mois
- Tâches et groupes de tâches hiérarchiques (3 niveaux)
- Drag & drop des barres : déplacement horizontal et redimensionnement (début/fin)
- Création de dépendances par glisser-déposer entre barres
- Suppression de dépendances au survol
- Flèches de dépendances avec courbes de Bézier

### Calendrier
- Jours fériés français intégrés (calendrier perpétuel, algorithme de Pâques)
- Week-ends grisés, masquage optionnel
- Ligne "Aujourd'hui" en surbrillance
- Calcul automatique en jours ouvrés

### Planification automatique
- Auto-planification par dépendances (tri topologique de Kahn)
- Calcul du Chemin Critique (CPM — méthode PERT)
- Mise à jour automatique des groupes (dates min/max des enfants)

### Gestion financière
- Montant par tâche + montant à l'avancement (calculé selon %)
- Modal de facturation avec KPI : budget total, réalisé, reste
- Totaux par groupe et projet

### Export / Import
- **Export Excel (.xlsx)** — généré sans dépendance externe (ZIP + XLSX natifs)
  - Onglet Gantt visuel coloré avec volets figés
  - Onglet Données complet
  - Onglet Facturation
- **MS Project** — import/export au format MSPDI XML (compatible 2007–2021)

### Interface
- Thème sombre / clair (🌙 / ☀️) avec persistance
- Tooltip au survol après 1,5 s, ancré à la barre
- Barre de statistiques : tâches, durée, avancement, budget
- Réordonnancement par drag & drop dans la liste
- Raccourcis clavier : `N` (nouvelle tâche), `Del` (supprimer), `Esc` (fermer)

---

## Utilisation

Ouvrir `ganttflow.html` directement dans un navigateur moderne (Chrome, Firefox, Edge, Safari).

**Aucune installation requise. Aucun serveur. Aucune dépendance.**

Les données sont persistées dans le `localStorage` du navigateur.

---

## Structure du fichier

```
ganttflow.html          ← Application complète (HTML + CSS + JS)
```

Tout est contenu dans un seul fichier HTML (~142 Ko).

---

## Compatibilité

| Navigateur | Support |
|---|---|
| Chrome / Chromium 90+ | ✅ Complet |
| Firefox 88+ | ✅ Complet |
| Edge 90+ | ✅ Complet |
| Safari 14+ | ✅ Complet |

Fonctionne en **mode hors-ligne** — les polices Google Fonts sont chargées de manière non-bloquante avec fallback système.

---

## Raccourcis clavier

| Touche | Action |
|---|---|
| `N` | Nouvelle tâche |
| `G` | Nouveau groupe |
| `Del` | Supprimer la tâche sélectionnée |
| `Esc` | Fermer le modal |
| `Enter` | Valider le champ durée |

---

## Interactions Gantt

| Action | Geste |
|---|---|
| Déplacer une barre | Cliquer-glisser sur la barre |
| Modifier le début | Poignée gauche de la barre |
| Modifier la fin | Poignée droite de la barre |
| Créer une dépendance | Glisser depuis le point bleu (survol 1,5 s) |
| Supprimer une dépendance | Survoler la flèche 1,5 s → bouton × |
| Ouvrir le détail | Double-clic sur la barre |

---

## Licence

MIT — libre d'utilisation, de modification et de distribution.
