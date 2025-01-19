+++
title = "Showcase"
date = "2025-01-19"
author = "Louis"
hideComments = true
+++

## Tempobot EDF - Votre assistant énergétique ⚡

Tempobot EDF est un bot Discord couplé à un site web interactif, conçu pour fournir des informations fiables et en temps réel sur les alertes Tempo d'EDF. Avec un système de notifications personnalisées et des commandes simples, vous êtes toujours informé des jours bleus, blancs et rouges, ainsi que des meilleures périodes pour consommer.

## Fonctionnalités principales 🛠️

- Prévisions pour demain :
  Consultez les prévisions Tempo de la journée suivante pour anticiper vos besoins.

- Site web dédié :
  Accédez à un tableau de bord simple pour visualiser l'historique des jours Tempo, consulter les détails des couleurs, et personnaliser vos notifications.

- Notifications par ntfy.sh :
  Intégration avec ntfy.sh pour des alertes rapides directement sur vos appareils.

## Exemple de code d'intégration 💻

Voici un extrait du code :

```javascript
import fetch from "node-fetch";

async function getTodayTempo() {
  try {
    const response = await fetch(
      "https://www.api-couleur-tempo.fr/api/jourTempo/today"
    );
    const data = await response.json();

    const colorMap = {
      1: "🔵 Bleu",
      2: "⚪️ Blanc",
      3: "🔴 Rouge",
    };

    const color = colorMap[data.codeJour] || "Inconnu";
    return `Aujourd'hui, la couleur Tempo est : **${color}**.`;
  } catch (error) {
    return "Erreur : Impossible de récupérer la couleur Tempo du jour.";
  }
}
```

## Le site web 🌐

Tempobot EDF est accompagné d'un site moderne et intuitif :

- URL : tempobot.example.com
- Fonctionnalités : [https://tempobotsite.onrender.com/](https://tempobotsite.onrender.com/)
- - Historique des jours Tempo.
- - Tutoriels pour comprendre le fonctionnement du système Tempo.
- - Interface de personnalisation des alertes.
