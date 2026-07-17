# Grafana Partner Assessment Engine

Outil interne d'évaluation objective d'un partenaire Grafana Labs selon quatre dimensions : **Skill · Scale · Will · Strategic Fit**.

Application autonome, sans dépendance ni build : tout tient dans `index.html` et tourne 100 % en local dans le navigateur. Aucune donnée n'est envoyée sur le réseau ; l'état est sauvegardé via `localStorage`.

## Utilisation

Ouvrir `index.html` dans un navigateur (garder le dossier `assets/` à côté pour le logo).

## Fonctionnalités

- **6 écrans** : Profil, Évaluation, Décision, Prép. Meeting, Plan d'activation, Portfolio.
- **Moteur de scoring** sur 100 pts (Skill 30 · Scale 25 · Will 30 · Fit 15) avec règle « déclaré vs prouvé », bonus « pépite » et red flags (pénalités, dont un red flag disqualifiant qui plafonne le score).
- **Score de confiance** et badge « provisoire » quand moins de 50 % des critères sont renseignés.
- **Preuve/justification par critère** (lien, certification, référence client), reprise dans le rapport.
- **Suggestions de red flags** déduites du profil (non destructives).
- **Radar** des 4 piliers, **jauge** de score, barres de progression.
- **Portfolio** : matrice Potentiel × Volonté, comparaison radar multi-partenaires, historique du score (sparkline), export CSV.
- **Exports** : JSON (backup/partage), rapport PDF (impression), brief meeting en Markdown / presse-papier.

## Structure

```
index.html      Application complète (HTML + CSS + JS)
assets/         Logo Grafana Labs
```

## Modèle de scoring

| Dimension       | Poids | Max |
|-----------------|-------|-----|
| Skill           | 30 %  | 30  |
| Scale           | 25 %  | 25  |
| Will            | 30 %  | 30  |
| Strategic Fit   | 15 %  | 15  |

Classification finale : Strategic Growth Partner (≥85), High-Potential (≥70), Incubate (≥55), Referral (≥40), Do Not Prioritize (<40).

---

Prototype interne. Non affilié officiellement à Grafana Labs.
