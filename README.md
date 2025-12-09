# DSS-Contact Manager 

Der **DSS-Contact Manager** ist ein einfaches, menügesteuertes Kontaktbuch, das es Nutzern ermöglicht, interaktiv persönliche Kontaktdaten zu erfassen, zu bearbeiten, zu suchen und zu löschen. Die Benutzereingaben werden sinngemäss validiert und anschliessen auf Befehl des Nutzers gespeichert. 
Zu jedem Kontakt können folgende Informationen gespeichert werden:

- Name
- Telefonnummer
- E-Mail-Adresse
- Wohnadresse

Alle Daten werden lokal gespeichert und beim Programmstart wieder eingelesen. Das Programm ist ideal für Personen, die ihre Kontakte übersichtlich und schnell zugänglich verwalten möchten.

---
## 📌 Motivation

Kommunikation ist ein zentraler Bestandteil des modernen Arbeits- und Studienalltags. Besonders zum Start eines neuen Lebensabschnitts, wie einem Studium, lernt man viele neue Menschen kennen. Ein digitales Kontaktbuch hilft dabei, diese Kontakte systematisch zu erfassen, zu behalten und langfristig zu pflegen.

Der DSS Contact Manager unterstützt Benutzer dabei, schnell und unkompliziert auf ihre wichtigsten Kontakte zuzugreifen – jederzeit und ohne externe Plattform.

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
python main.py  oder  python DSS_COntact_Manager.py
```

Falls die Datei anders heisst, entsprechend anpassen.

🖼️ Screenshots (Platzhalter)

Füge hier später eure eigenen Screenshots ein:

Hauptmenü

Kontakte anzeigen

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

## 🧑‍💻 Beispiel: Menüführung (Nutzer-Ansicht)
```text
=== DSS-CONTACT MANAGER ===

1. Kontakt hinzufügen
2. Alle Kontakte anzeigen
3. Kontakt aktualisieren
4. Kontakt löschen
5. Kontakt suchen
6. Programm beenden

Bitte wählen Sie eine Option:
```


## 📝 Beispielcode: Kontakt hinzufügen
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

## ⚙️ Installation & Start
Voraussetzungen:
- Python 3.x installiert
- Projektdateien lokal gespeichert

Starten des Programms:
```text
python main.py
```

Falls die Datei anders heisst, entsprechend anpassen.

🖼️ Screenshots (Platzhalter)

Füge hier später eure eigenen Screenshots ein:

Hauptmenü

Kontakte anzeigen

----
## 🚧 Herausforderungen während der Entwicklung

Da dies ein Einsteigerprojekt ist, lagen die grössten Schwierigkeiten in:
der Eingabevalidierung dem Umgang mit Schleifen und Booleschen Bedingungen
dem strukturierten Datei-Einlesen und -Schreibe Menüführung mit wiederholter Benutzerinteraktion

Durch konsequente Anwendung der Unterrichtsmaterialien konnten diese Herausforderungen Schritt für Schritt gelöst werden.

----
## 👥 Projektteam-Beteiligte

> Dario Ardito

> Sharun Sivaneswaran

> Steven Momo
