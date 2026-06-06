# FreshFlow Dashboard 📊

Dashboard de pilotage interactif pour la gestion de projet **FreshFlow** (GreenBasket).

## 🚀 Utilisation

**Aucune installation requise !** Ouvrez simplement `index.html` dans votre navigateur.

```bash
# Option 1 : Double-cliquez le fichier
index.html

# Option 2 : Avec Live Server (VS Code)
# Clic droit → "Open with Live Server"

# Option 3 : Terminal
python -m http.server 8000
# Puis ouvrez http://localhost:8000
```

## ✨ Fonctionnalités

### 📈 Dashboards
- **Métriques Clés** : 3 héros cards avec compteurs animés
- **KPI Grid** : 7 cartes KPI avec progress bars, statuts colorés
- **Graphiques** :
  - 📉 Sprint avancement (ligne)
  - 🍩 Donut répartition statuts KPIs
  - 📊 Budget par poste (barres empilées)
- **Timeline** : Jalons critiques (J+75, J+90, J+113)
- **Tableau filtrable** : Tous/Vert/Orange/Rouge
- **Prédictions** : Fin avancement, budget estimé, Go/No-Go dates

### 🎯 Interactions
✅ **Éditer KPI** — Clic sur une card → modal d'édition  
✅ **Auto-save** — Valeurs sauvegardées en localStorage  
✅ **Copier Slack** — Bouton pour copier alerte formatée  
✅ **Exporter** — Télécharger rapport .txt complet  
✅ **Filtre tableau** — Statuts Vert/Orange/Rouge  
✅ **Animations** — Stagger fade-in, progress bars, pulse rouge  

### 🚨 Alerte Bloquante
Bandeau **WeWeb offline** avec animation clignotante permanente (blink + pulse)

## 🎨 Design

- **Thème** : Dark industriel (#0a0f0d) + accents vert (#4ade80) & ambre (#fbbf24)
- **Typos** : DM Mono + Instrument Sans (Google Fonts)
- **Responsive** : Mobile-friendly grid auto-fit
- **Pas de dépendances locales** — Tout via CDN (Chart.js 4.4.1)

## 💾 Données Mockées

7 KPIs avec statut automatique (Vert/Orange/Rouge) :

1. **Avancement Technique** (45%) → Orange
2. **Budget Consommé** (3280€) → Vert ✓
3. **Précision IA** (70%) → Vert ✓
4. **Gaspillage Léa** (11.2%) → Orange
5. **Workflows Make.com** (15/20) → Orange
6. **Engagement Léa** (60%) → Orange
7. **Offline WeWeb** (BLOQUANT) → **ROUGE 🚨**

**localStorage** : Toutes les éditions KPI sont automatiquement sauvegardées et restaurées au rechargement.

## 📝 Éditer les données

Les données sont en dur dans le `<script>` (section `/* DATA */`). Pour modifier :

```javascript
const KPI_DATA_DEFAULT = [
  {
    id: 1,
    nom: "Mon KPI",
    valeur: 45,
    cible: 100,
    // ...
  }
]
```

Les données éditées via le dashboard sont sauvegardées en localStorage et prennent priorité sur les valeurs par défaut.

## 🔧 Technologie

- **HTML5 sémantique**
- **CSS3 custom properties** + Grid/Flexbox
- **Vanilla JS** (zéro dépendances locales)
- **Chart.js 4.4.1** via CDN
- **Google Fonts** (DM Mono + Instrument Sans)
- **LocalStorage API** pour persistance

## 📱 Responsive

Adapté pour :
- 🖥️ Desktop (1400px+)
- 💻 Laptop (1024px)
- 📱 Tablet (768px)
- 📱 Mobile (< 600px)

Timeline passe en mode vertical sur mobile.

## 🎓 Contexte Pédagogique

Dashboard créé pour la formation **Oreegami — Bloc 2 Product Builder no-code & IA générative**.

Cas d'usage : Pilotage d'un projet no-code de gestion des stocks (FreshFlow) pour une chaîne de 25 magasins bio (GreenBasket).

**Contexte fictif** : J+45 / 120 jours totaux, budget 15k€, équipe 4 personnes.

---

**Questions ?** Consultez la [source code](index.html) — code bien commenté en français.
