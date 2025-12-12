# <img width="601" height="199" alt="image" src="https://github.com/user-attachments/assets/c36131a6-7c13-413c-8a7f-af3c848d03e8" />

Der **DSS-Contact Manager** ist ein einfaches, menügesteuertes Kontaktbuch, das es Nutzern ermöglicht, interaktiv persönliche Kontaktdaten zu erfassen, zu bearbeiten, zu suchen und zu löschen. Die Benutzereingaben werden sinngemäss validiert und anschliessend auf Befehl des Nutzers gespeichert. 
Zu jedem Kontakt können folgende Informationen gespeichert werden:

- Name
- Telefonnummer
- E-Mail-Adresse
- Wohnadresse

Alle Daten werden lokal gespeichert und beim Programmstart wieder eingelesen. Das Programm ist ideal für Personen, die ihre Kontakte übersichtlich und schnell zugänglich verwalten möchten.

---
## 📌 Motivation

Kommunikation ist ein zentraler Bestandteil des modernen Arbeits- und Studienalltags. Besonders zum Start eines neuen Lebensabschnitts, wie einem Studium, lernt man viele neue Menschen kennen. Ein digitales Kontaktbuch hilft dabei, diese Kontakte systematisch zu erfassen, zu behalten und langfristig zu pflegen.

Der DSS-Contact Manager unterstützt Benutzer dabei, schnell und unkompliziert auf ihre wichtigsten Kontakte jederzeit und ohne externe Plattform zuzugreifen.

---
## 🎯 Zielgruppe

Die Anwendung richtet sich an alle Personen, die:

- regelmässig Kontakte verwalten,
- schnell auf Kontaktinformationen zugreifen möchten,
- eine einfache, übersichtliche Nutzerführung bevorzugen.

---
## ⚙️ Installation & Start
Voraussetzungen:
- Python 3.x installiert
- Projektdateien lokal gespeichert

Starten des Programms:
```text
python main.py
```
oder
```text
python DSS_Contact_Manager.py
```
---
## 🏛️ Die Architektur

Im folgenden Bild werden die einzelnen Module des Kontaktbuches dargestellt und dessen Kommunikation untereinander:

<img width="548" height="451" alt="image" src="https://github.com/user-attachments/assets/9c759925-a400-4170-92db-3e42dc9efb7b" />

---
## 📂 Hauptfunktionen
Der DSS-Contact Manager bietet folgende Funktionen:

1. **Kontakt hinzufügen**  
2. **Alle Kontakte anzeigen**  
3. **Kontakt aktualisieren**  
4. **Kontakt löschen**  
5. **Kontakt suchen**  
6. **Programm beenden**

Alle Funktionen sind über ein benutzerfreundliches Menü erreichbar.

---
## 🧭 Programmablauf
```text
Programmstart
    ↓
HAUPTMENÜ (Optionen 1–6)
    ↓
Benutzerwahl
    ↓
Ausführen der gewählten Funktion
    ↓
Anzeige / Bestätigung
    ↓
Zurück zum HAUPTMENÜ
    ↓
Beenden → Daten speichern → Programmende
```
---

## Beispiele: 
### 🧑‍💻 Menüführung (Nutzer-Ansicht)
```text
=== DSS-CONTACT MANAGER ===

1. Kontakt hinzufügen
2. Alle Kontakte anzeigen
3. Kontakt aktualisieren
4. Kontakt löschen
5. Kontakt suchen
6. Programm beenden

Bitte wählen Sie eine Option:__
```


## 📝 Code: Kontakt hinzufügen (Administrators-Ansicht)
```text
def kontakt_hinzufügen():
    print("\n--- Neuen Kontakt hinzufügen ---")
    name = input("Name: ").strip()

    while not name:
        print("Name darf nicht leer sein.")
        name = input("Name: ").strip()

    phone = input("Telefonnummer: ").strip()
    while not phone.isdigit():
        print("Telefonnummer darf nur Zahlen enthalten.")
        phone = input("Telefonnummer: ").strip()

    email = input("E-Mail: ").strip()
    while "@" not in email:
        print("Ungültige E-Mail-Adresse. Muss ein '@' enthalten.")
        email = input("E-Mail: ").strip()

    address = input("Adresse: ").strip()

    contacts.append({
        "name": name,
        "phone": phone,
        "email": email,
        "address": address
    })

    print("\nKontakt wurde erfolgreich gespeichert!")
```
----

## 🧪 Datenvalidierung
Das Programm überprüft Benutzereingaben systematisch:

Name darf nicht leer sein

Telefonnummer darf nur Zahlen enthalten

E-Mail-Adresse muss ein @ enthalten

Ungültige Menüeingaben führen zu klaren Fehlermeldungen und erneuter Eingabeaufforderung

Dies erhöht die Stabilität der Anwendung und verhindert fehlerhafte Datensätze.

----
## 🚧 Herausforderungen während der Entwicklung

Da es sich um ein Einsteigerprojekt handelt, traten verschiedene Herausforderungen auf. Besonders anspruchsvoll waren die Eingabevalidierung sowie der Umgang mit Schleifen und booleschen Bedingungen. Weitere Schwierigkeiten ergaben sich beim strukturierten Datei-Einlesen und Schreiben sowie bei der Menüführung mit wiederholter Benutzerinteraktion.

Dank anwenderfreundlichen Skrips, der Unterstützung meiner Klassenkammeraden und KI konnten Fragen und Unklarheiten zu einem grossen Teil geklärt werden. Dadurch liessen sich die Herausforderungen Schritt für Schritt erfolgreich bewältigen. Die letzten kritische Punkte wurden beim Coaching mit dem Dozent geklärt und 

----
## 👥 Projektteam-Beteiligte

> Dario Ardito

> Sharun Sivaneswaran

> Steven Momo
