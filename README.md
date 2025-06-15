# 🧠 Bachelorarbeit – Konzeptuelle Spezialisierung in Beschreibungslogik (EL)

## 📘 Thema
Diese Bachelorarbeit beschäftigt sich mit der **Berechnung minimaler Generalisierungen und Spezialisierungen** von Konzepten in der **Beschreibungssprache EL**. Ziel ist es, formale Methoden zu entwickeln, um konzeptuelle Nachbarn (sowohl obere als auch untere) effizient zu bestimmen – ein zentrales Thema in der Ontologiebearbeitung und wissensbasierten Systemen.

---

## 🧩 Idee der Arbeit

In wissensbasierten Systemen und Ontologien ist es oft notwendig, zwischen Konzepten zu generalisieren oder zu spezialisieren. Dafür betrachtet diese Arbeit:
- **Minimale Generalisierungen (Upper Neighbors)**: Die direkt allgemeineren Konzepte eines gegebenen Konzepts.
- **Minimale Spezialisierungen (Lower Neighbors)**: Die direkt spezielleren Konzepte eines gegebenen Konzepts.

Diese Operationen ermöglichen:
- die **strukturelle Navigation** in Konzept-Hierarchien,
- das **Verstehen von Ähnlichkeiten** zwischen Konzepten,
- und die **Bereinigung oder Erweiterung** von Ontologien.

---

## ⚙️ Implementierung

Die Arbeit enthält eine Python-Implementierung der folgenden Kernfunktionen:

- `compute_upper_neighbors(concept)`: Berechnet die direkt übergeordneten Konzepte.
- `compute_lower_neighbors(concept)`: (optional, je nach Umfang) Berechnet die direkt untergeordneten Konzepte.
- `reduce(concept)`: Führt semantische Normalisierung eines Konzepts durch.
- Unterstützung für folgende EL-Konzepte:
  - `ConceptName`: Einfache Konzepte wie `Person`, `Student`, etc.
  - `ExistentialRestriction`: Einschränkungen wie `∃hasPart.Organ`
  - `Conjunction`: Verknüpfungen wie `Student ⊓ ∃hasPet.Dog`

Die Ausgabe der `reduce`-Funktion ist stets eine **Konjunktion**, und daher basieren alle weiteren Berechnungen auf dieser strukturierten Form.
