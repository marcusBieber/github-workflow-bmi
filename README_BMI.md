# BMI Rechner

Dieses Projekt ist eine einfache BMI-Rechner-Webanwendung, die mit HTML, CSS, Bootstrap und JavaScript erstellt wurde. Zusätzlich beinhaltet es eine Express.js-Serverkomponente, um die Anwendung bereitzustellen. Die Anwendung unterstützt Continuous Integration (CI) durch automatische Tests sowie Continuous Deployment (CD) mit GitHub Actions.

## Funktionen

- Berechnung des Body-Mass-Index (BMI) basierend auf Gewicht und Größe
- Einfache UI mit Bootstrap für responsives Design
- Automatische Tests für die BMI-Berechnungslogik
- CI/CD-Pipeline mit GitHub Actions zur Automatisierung von Tests und Deployment

## Projektstruktur

```
📂 bmi-calculator
├── 📂 frontend
│   ├── index.html  # Haupt-UI der Anwendung
│   ├── main.js     # Logik für die BMI-Berechnung
│   ├── style.css   # (Optional) Stile für die UI
├── server.js       # Express.js-Server zur Bereitstellung der Anwendung
├── package.json    # Abhängigkeiten und Skripte
├── package-lock.json
├── README.md       # Projektbeschreibung
├── .github
│   ├── workflows
│   │   ├── ci.yml  # CI-Workflow für Tests
│   │   ├── cd.yml  # CD-Workflow für Deployment
└── tests
    ├── bmi.test.js # Unit-Tests für die BMI-Berechnung
```

## Installation und Lokales Deployment

### Voraussetzungen

- Node.js (empfohlen: v18 oder höher)
- npm (Node Package Manager)

### Schritte zur lokalen Ausführung

1. Repository klonen:
   ```sh
   git clone https://github.com/USERNAME/bmi-calculator.git
   cd bmi-calculator
   ```

2. Abhängigkeiten installieren:
   ```sh
   npm install
   ```

3. Server starten:
   ```sh
   node server.js
   ```

4. Die Anwendung ist jetzt unter `http://localhost:3000` erreichbar.

## Tests

Das Projekt enthält automatisierte Tests für die `calculateBMI`-Funktion.

Zum Ausführen der Tests:

```sh
npm test
```

## CI/CD

### Continuous Integration (CI)
Bei jedem Pull-Request gegen den `main`-Branch werden automatisierte Tests durchgeführt, um sicherzustellen, dass die `calculateBMI`-Funktion korrekt arbeitet.

### Continuous Deployment (CD)
Bei jedem Push auf den `main`-Branch wird die neueste Version der Anwendung automatisch auf eine EC2-Instanz deployt.

Das Deployment umfasst:
- Verbindung zur EC2-Instanz über SSH
- Klonen oder Aktualisieren des Repositorys
- Installation der Abhängigkeiten
- Start der Anwendung mit `pm2` für eine dauerhafte Ausführung

## Autor

- **Dein Name** – [GitHub](https://github.com/USERNAME)

---

Dieses Projekt wurde als Übung für die Implementierung von CI/CD mit GitHub Actions erstellt.
