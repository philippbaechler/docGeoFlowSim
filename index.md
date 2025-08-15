---
layout: default
title: Physikalisch basierte Flutsimulation
---

# Physikalisch basierte Flutsimulation

Dieses Projekt simuliert die Ausbreitung von Wasser über ein digitales Höhenmodell (DEM). Dabei wird der Wasserstand für jeden Zeitschritt neu berechnet.

## Formel zur Geschwindigkeit

Die Fließgeschwindigkeit \(v\) ergibt sich nach der vereinfachten Manning-Gleichung zu:

\\[
v = \\frac{1}{n} h^{2/3} \\sqrt{S}
\\]

wobei:

- \(v\): Fließgeschwindigkeit [m/s]  
- \(n\): Rauigkeitsbeiwert (z. B. 0.03 für Beton)  
- \(h\): Wassertiefe [m]  
- \(S\): Hangneigung [-]  

## Beispielplot

<img src="https://drive.google.com/uc?export=view&id=1PtSKMzJWDPM_wp6dnS5OaW2ym7cpQw-_" alt="Simulationsergebnis" width="600">

## Fazit

Die Simulation erreicht eine stabile Verteilung des Wassers nach mehreren Schritten. Weitere Optimierungen wie eine zeitabhängige Flussberechnung oder Einbezug von Infiltration sind möglich.
