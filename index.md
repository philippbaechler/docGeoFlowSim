---

## layout: default title: "Physikalisch basierte Flutsimulation mit Python" description: "Ein Blogpost zur Modellierung von Wasserverteilung mit DEM-Daten und Fließgeschwindigkeit"

# 🌊 Physikalisch basierte Flutsimulation mit Python

**Autor:** Dein Name
**Datum:** 2025-06-21

## 🔍 Motivation

In diesem Projekt untersuche ich, wie sich Wasser über ein digitales Höhenmodell (DEM) verteilt, wenn es an einem bestimmten Punkt eingeleitet wird. Ziel ist es, eine realitätsnahe, zeitschrittbasierte Flutsimulation zu entwickeln, bei der auch die Fließgeschwindigkeit des Wassers (basierend auf dem Gefälle und der Wassertiefe) berücksichtigt wird.

## 🧬 Simulationsidee

Die Simulation basiert auf folgenden physikalischen Konzepten:

* **Wasserhöhe:** Die Verteilung des Wassers basiert auf der Differenz des *Gesamthöhenpotenzials* zwischen benachbarten Zellen.
* **Fließgeschwindigkeit:** Die Geschwindigkeit des Wassers wird mit der **Gauckler-Manning-Formel** berechnet:

```math
v = \frac{1}{n} \cdot h^{2/3} \cdot \sqrt{S}
```

## 💪 Setup

### 📆 Benötigte Pakete

```bash
pip install numpy scipy matplotlib pillow
```

### 📁 Dateistruktur

* `DEM_data/mini.tif`: dein digitales Höhenmodell (Graustufenbild)
* `flood_simulation.py`: das Hauptskript

## 🔮 Simulationscode

Den gesamten Simulationscode findest du [hier im Repository](https://github.com/deinname/flood-simulation).

## 📊 Beispielresultate

Hier einige Beispielbilder, die den Flussverlauf alle 10 Schritte zeigen:

&#x20; &#x20;

## ⏲ Zeitschrittberechnung (optional)

Die reale Dauer eines Zeitschritts ergibt sich näherungsweise durch:

```math
\Delta t = \frac{\text{Zellgröße}}{\max(\text{Wassergeschwindigkeit})}
```

Momentan wird pro Iteration ein fixer Zeitschritt angenommen.

## ⚖️ Nächste Schritte

* Implementierung von **Regenereignissen** oder **Dauerregen**
* Anbindung an **radarbasierte Niederschlagsdaten**
* Echtzeit-Simulation mit PyGame oder WebGL

## 📅 GitHub-Repository

👉 [github.com/deinname/flood-simulation](https://github.com/deinname/flood-simulation)

## 💪 Fazit

Diese Simulation zeigt, wie mit einfachen physikalischen Prinzipien und Python-Bibliotheken eine realitätsnahe Wasserverteilung über Gelände modelliert werden kann.
