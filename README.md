# m164_PortFolio_Eli_Can
This repsository was created for "the modul 164".
# Projektdokumentation – Datenmodellierung & SQL

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

![Alternativtext](https://gitlab.com/ch-tbz-it/Stud/m164/-/raw/main/x_res/m164_modul%C3%BCbersicht-Theorie.drawio.png)

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

![Alternativtext](https://gitlab.com/ch-tbz-it/Stud/m164/-/raw/main/2.Tag/media/213e861ebd732e0ed4f44ca81930149a.png)


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

![Alternativtext](https://gitlab.com/ch-tbz-it/Stud/m164/-/raw/main/3.Tag/media/Einfache_Hierarchie.png)


- Statt rekursiver FK in derselben Tabelle wird eine **Verknüpfungstabelle** genutzt.
- Beispiel: `Kategorie_Hierarchie(ElternID, KindID)`

#### Stücklistenproblem (Bill of Materials – BOM)

![Alternativtext](https://gitlab.com/ch-tbz-it/Stud/m164/-/raw/main/3.Tag/media/a23bd48e09ca11406474760f63e8d173.png)


- Ziel: Ermittlung aller elementaren Bestandteile eines Produkts
- Beispiel: Ein Fahrrad besteht aus Rahmen, Rädern etc., diese wiederum aus Felgen, Speichen usw.
- Rekursive Struktur wird verwendet, um verschachtelte Komponenten zu berechnen

### Tag 3 Reflexion

Ich konnte heute viele verschiedene Themen bearbeiten. Allerdings war ich etwas enttäuscht, dass ich nicht mehr Zeit für meine Notizen hatte, da die Aufgaben viel Zeit in Anspruch nahmen. Trotzdem konnte ich zu jedem Thema Notizen anfertigen.

---

## Tag 4

### Tag 4 Notizen

| Beziehungstyp (logisch)    | MasterTab.links → DetailTab.rechts | Möglich | Nicht möglich / wird zu        | Constraints FK             |
|----------------------------|-------------------------------------|---------|--------------------------------|----------------------------|
| **eins zu eins**           | 1:c, c:c                            | 1:1     | ➔ 1:c                          | `NOT NULL`, `UNIQUE`       |
| **eins zu viele**          | 1:mc, c:mc                          | 1:m     | ➔ 1:mc<br>c:m ➔ c:mc           | `NOT NULL`                 |
| **viele zu viele**         | m:m, m:mc, mc:m, mc:mc              | –       | ➔ 1:mc – [TT] – mc:1           | `NOT NULL` auf beiden FKs  |

---

#### JOINs 

Wenn man Daten aus mehreren Tabellen zusammenbringen will, braucht man JOINs. JOINs verbinden Tabellen über gemeinsame Werte – meistens über Primär- und Fremdschlüssel.

- **`INNER JOIN`**  
  Zeigt **nur Datensätze**, die in **beiden Tabellen** vorkommen.  
  Wenn ein Kunde keine Bestellung gemacht hat, sieht man ihn nicht.

- **`LEFT JOIN`**  
  Zeigt **alle** aus der **linken Tabelle**, auch wenn es rechts kein Match gibt.  
  Fehlende Werte auf der rechten Seite werden mit `NULL` ergänzt.

- **`RIGHT JOIN`**  
  Umgekehrt: Alle aus der **rechten Tabelle** werden gezeigt, auch ohne Match links.

- **`FULL OUTER JOIN`**  
  (Nicht in jedem System verfügbar):  
  Zeigt alles – aus beiden Tabellen – auch wenn es keine Übereinstimmungen gibt.

---

### Tag 4 Reflexion

Heute war’s ehrlich gesagt der stressigste Tag bisher, weil wir auch noch die LB1 hatten. Deshalb konnte ich im Vergleich zu den letzten Tagen nicht alles lösen, was ich wollte. Trotzdem habe ich zu den wichtigsten Sachen Notizen gemacht und an den Aufträgen gearbeitet. Ich bin heute nicht wirklich zufrieden mit meiner Leistung, aber das nehme ich mit nächstes Mal geb ich mir mehr Mühe und plane besser vor.

---

## Tag 5

### Tag 5 Notizen

## Funktionen, die häufig mit `GROUP BY` verwendet werden

- **COUNT**  
  Gibt die Anzahl der Zeilen zurück.

- **SUM**  
  Berechnet die Summe der Werte insgesamt.

- **AVG**  
  Berechnet den Durchschnitt.

- **MIN**  
  Gibt den kleinsten Wert zurück.

- **MAX**  
  Gibt den grössten Wert zurück.

---

## Datenintegrität

Datenintegrität stellt sicher, dass Daten in der Datenbank korrekt, konsistent und vollständig bleiben. Sie umfasst mehrere Aspekte:

- **Eindeutigkeit & Konsistenz:** Kein doppelter oder unerwarteter Datenverlust  
- **Referenzielle Integrität:** Beziehungen zwischen Tabellen bleiben gültig (z. B. eine Bestellung ist nur mit existierendem Kunden möglich)  
- **Datentypen & Beschränkungen:** Daten müssen im richtigen Format gespeichert werden  
- **Validierung:** Daten werden vor der Speicherung geprüft  

---

## Referenzielle Integrität

Referenzielle Integrität bedeutet, dass die Beziehungen zwischen Tabellen stets gültig sind. Dazu gehören:

- **FK-Constraints:** Verhindern ungültige oder inkonsistente Verknüpfungen  
- **Lösch- und Update-Regeln:** Steuern, wie sich Änderungen an Primärschlüsseln auf abhängige Tabellen auswirken  
- **Langfristige Konsistenz:** Sicherstellung, dass historische und aktuelle Daten korrekt abrufbar bleiben  

---

### Tag 5 Reflexion

Heute konnte ich erneut sehr viel lernen und habe vieles mitgenommen. Ich bin davon überzeugt, dass alles, was ich heute gelernt habe, äusserst wichtig für das LB2 ist. Deshalb gebe ich mir grosse Mühe, alles wirklich zu verstehen. Insgesamt konnte ich heute auch viel praktisch austesten, worüber ich sehr glücklich bin.

---
## Tag 6

### Tag 6 Notizen

#### **SUBQUERY (SUBSELECT / Unterabfrage)**

Ein Subselect in einer MySQL-Datenbank ist eine Abfrage **innerhalb einer anderen Abfrage**.

![Alternativtext](https://gitlab.com/ch-tbz-it/Stud/m164/-/raw/main/6.Tag/media/Nicht_Skalar.png)

---

#### Skalare Unterabfrage

Hier ist ein Beispiel für eine **skalare SELECT-Abfrage** mit einer Subquery:


SELECT city_destination, ticket_price, travel_time, transportation 
FROM one_way_ticket
WHERE ticket_price < (
    SELECT MIN(ticket_price) 
    FROM one_way_ticket
    WHERE city_destination = 'Bariloche' AND city_origin = 'Paris'
)
AND city_origin = 'Paris';

Nicht-skalare Unterabfrage

Hier ist ein Beispiel für eine **nicht-skalare SELECT-Abfrage** mit einer Subquery:

USE subselect;

SELECT name, age, country
FROM users
WHERE country IN (
    SELECT name 
    FROM country 
    WHERE region = 'Europa'
);

### Tag 6 Reflexion

Heute war ich mehrheitlich mit dem praktische unterwegs, also in Verhleich uz den anderen Tagne habe ich viel weniger Theorie durchgenommen, was mich leicht unsicher macht aber in der Prüfung hat das prakstische Teil mehr Punkte, deshalb bin auch okay damit. Insegesamt war ich heute sehr produktiv.

---

## Tag 7

### Tag 7 – Notizen

#### Datensicherung von Datenbanken

Datenbanksysteme spielen eine grosse Rolle – sei es für das Speichern von schützenswerten Kundendaten oder Produktinformationen. Weil diese Daten so wichtig sind, müssen sie gesichert und geschützt werden.

#### Möglichkeiten zur Sicherung von Datenbanken

- **Voll-Backup:**  
  Hier geht es um ein komplettes Backup, welches sehr kostenintensiv ist und eine riesige Kapazität verbraucht. Dafür hat man jedoch eine Sicherung des gesamten Produkts.

- **Differentielles Backup:**  
  Hier werden nur die Daten gespeichert, die sich verändert haben. Im Gegensatz zum Voll-Backup ist dies kostengünstiger, da nicht mehr alles nochmals gespeichert wird, sondern nur die aktualisierten Daten.

- **Inkrementelles Backup:**  
  Hier werden nur die Daten gespeichert, die neu sind oder geändert wurden. Im Unterschied zur differentiellen Methode bezieht sich ein inkrementelles Backup immer auf das vorherige (sowohl auf das Voll-Backup als auch auf das letzte inkrementelle Backup). Dadurch spart man Speicherplatz – und somit auch Geld.

---

### Tag 7 – Reflexion

Ich hatte dieses Thema schon einmal, daher war es für mich mehrheitlich nichts Neues. Aus diesem Grund habe ich meine Zeit heute grösstenteils dafür genutzt, ältere Themen zu wiederholen. Trotzdem habe ich auch zu diesem Thema Notizen gemacht.  
Mit meiner heutigen Leistung bin ich zufrieden.


---

## Tag 8 – Reflexion

Insgesamt lief heute alles gut, da es die letzte Stunde vor der Prüfung ist habe ich mich auf die vergangen Aufgaben fokusiert und habe auch die Musterprüfung gelöst. 
Ich habe keine Notizen erstellt, da es heute kein neues Thema gab.

