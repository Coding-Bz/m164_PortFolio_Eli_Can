# m164_PortFolio_Eli_Can
This repsository was created for "the modul 164".
# 📘 Projektdokumentation – Datenmodellierung & SQL

## Inhaltsverzeichnis

- [Tag 1 – Datenmodellarten](#tag-1--datenmodellarten)
  - [Notizen](#tag-1-notizen)
  - [Reflexion](#tag-1-reflexion)
- [Tag 2 – Generalisierung & Beziehungen](#tag-2--generalisierung--beziehungen)
  - [Notizen](#tag-2-notizen)
  - [Reflexion](#tag-2-reflexion)
- [Tag 3 – Hierarchien & Stücklisten](#tag-3--hierarchien--stücklisten)
  - [Notizen](#tag-3-notizen)
  - [Reflexion](#tag-3-reflexion)
- [Tag 4](#tag-4)
  - [Notizen](#tag-4-notizen)
  - [Reflexion](#tag-4-reflexion)
- [Tag 5](#tag-5)
  - [Notizen](#tag-5-notizen)
  - [Reflexion](#tag-5-reflexion)
- [Tag 6](#tag-6)
  - [Notizen](#tag-6-notizen)
  - [Reflexion](#tag-6-reflexion)
- [Tag 7](#tag-7)
  - [Notizen](#tag-7-notizen)
  - [Reflexion](#tag-7-reflexion)
- [Tag 8 – Abschluss](#tag-8--abschlussreflexion)

---

## Tag 1 – Datenmodellarten

### Tag 1 Notizen

_Bild-Link folgt._

In der Datenmodellierung gibt es drei verschiedene Datenmodelle, die aufeinander aufbauen:

#### Konzeptionelles Datenmodell
- Englisch: ERM (Entity Relationship Model)
- Dient der oberflächlichen Modellierung von Entitäten und deren Beziehungen (z. B. 1:n, m:n).

#### Logisches Datenmodell
- Englisch: ERD (Entity Relationship Diagram)
- Erweiterung des ERM mit Primärschlüsseln, Fremdschlüsseln und notwendigen Attributen.

#### Physisches Datenmodell
- Zeigt die konkrete Umsetzung in SQL (z. B. `CREATE TABLE`, `DROP TABLE`).
- Meist als Skriptdatei realisiert.

#### Modellierung in der 3. Normalform
- Ziel: Redundanz vermeiden und Datenbestände vor Anomalien schützen.
- Mittels Constraints wird die referenzielle Integrität sichergestellt.

### Tag 1 Reflexion

Heute ging es darum, die Grundlagen der Datenmodellierung zu wiederholen. Ich konnte alle Aufträge lösen. Die Herausforderung bestand darin, dass die Modellierung stark von individuellen Präferenzen beeinflusst wird, was Unsicherheit erzeugte. Deshalb habe ich aktiv Feedback von der Lehrperson eingeholt und dieses umgesetzt. Insgesamt bin ich mit meiner Leistung zufrieden.

---

## Tag 2 – Generalisierung & Beziehungen

### Tag 2 Notizen

_Bild-Link folgt._

#### Generalisierung
- Mehrere ähnliche Entitäten werden zu einer gemeinsamen Oberklasse zusammengefasst.
- Beispiel: *Student* und *Dozent* → *Person*

#### Spezialisierung
- Umgekehrter Vorgang: Eine allgemeine Entität wird in spezifische Unterklassen aufgeteilt.
- Beispiel: *Person* → *Kunde*, *Mitarbeiter*

#### Beziehungsarten

**Identifying Relationship**
- Starke Abhängigkeit
- Fremdschlüssel ist Teil des Primärschlüssels
- Child-Entity kann nicht ohne Parent-Entity existieren

**Non-Identifying Relationship**
- Fremdschlüssel ist **nicht** Teil des Primärschlüssels
- Child-Entity kann unabhängig existieren

#### DBMS – Datenbankmanagementsystem

**Vorteile:**
- Nutzung von Standards
- Effizienter Datenzugriff
- Kürzere Entwicklungszeit
- Hohe Flexibilität und Verfügbarkeit
- Wirtschaftlichkeit

**Nachteile:**
- Hohe Anfangsinvestitionen
- Zusätzliche Kosten für Sicherheit, Synchronisation, Konsistenz
- Allgemeine Software, nicht optimiert für Spezialfälle

#### DDL (Data Definition Language)
- `CREATE`, `ALTER`, `DROP`, `RENAME`, `TRUNCATE`, `COMMENT`

### Tag 2 Reflexion

Im Vergleich zum Vortag konnte ich heute deutlich mehr Neues lernen. Ich habe alle Aufgaben gelöst und zu allen Themen Notizen angefertigt. Auch im Checkpoint konnte ich jede Frage beantworten. Insgesamt war ich heute sehr produktiv.

---

## Tag 3 – Hierarchien & Stücklisten

### Tag 3 Notizen

#### Mehrfachbeziehungen
- Zwei Tabellen haben mehrere unabhängige Beziehungen zueinander.
- Diese müssen eindeutig und aussagekräftig benannt werden.

#### Rekursion (strenge Hierarchie)
- Eine Entität hat eine Beziehung zu sich selbst.
- Beispiel: *Mitarbeiter* hat einen *Vorgesetzten*, der ebenfalls ein *Mitarbeiter* ist.
- **Strenge Hierarchie** = Keine Zyklen (z. B. niemand ist sein eigener Chef)

#### Einfache Hierarchie (mit Zwischentabelle)

_Visualisierung folgt._

- Statt rekursiver FK in derselben Tabelle wird eine **Verknüpfungstabelle** genutzt.
- Beispiel: `Kategorie_Hierarchie(ElternID, KindID)`

#### Stücklistenproblem (Bill of Materials – BOM)

_Visualisierung folgt._

- Ziel: Ermittlung aller elementaren Bestandteile eines Produkts
- Beispiel: Ein Fahrrad besteht aus Rahmen, Rädern etc., diese wiederum aus Felgen, Speichen usw.
- Rekursive Struktur wird verwendet, um verschachtelte Komponenten zu berechnen

### Tag 3 Reflexion

Ich konnte heute viele verschiedene Themen bearbeiten. Allerdings war ich etwas enttäuscht, dass ich nicht mehr Zeit für meine Notizen hatte, da die Aufgaben viel Zeit in Anspruch nahmen. Trotzdem konnte ich zu jedem Thema Notizen anfertigen.

---

## Tag 4

### Tag 4 Notizen

_Folgt._

### Tag 4 Reflexion

_Folgt._

---

## Tag 5

### Tag 5 Notizen

_Folgt._

### Tag 5 Reflexion

_Folgt._

---

## Tag 6

### Tag 6 Notizen

_Folgt._

### Tag 6 Reflexion

_Folgt._

---

## Tag 7

### Tag 7 Notizen

_Folgt._

### Tag 7 Reflexion

_Folgt._

---

## Tag 8 – Abschlussreflexion

_Folgt._

