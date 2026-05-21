# PV-Dashboard

Ein Dashboard zur Anzeige und Analyse von Photovoltaik-Daten.

## Projektbeschreibung

Das PV-Dashboard ruft aktuelle Photovoltaik-Daten aus einer externen URL ab,
bereinigt und speichert diese automatisch und berechnet relevante Metriken.
Die Ergebnisse werden in einem interaktiven Dashboard visualisiert.

## Projektstruktur

```
pv-dashboard/
├── backend/
│   ├── fetcher.py        # Datenabruf aus URL
│   ├── cleaner.py        # Datenbereinigung
│   ├── storage.py        # Datenspeicherung
│   └── calculator.py     # Berechnung von Metriken
├── frontend/
│   └── dashboard.py      # Streamlit Dashboard
├── tests/
│   ├── test_fetcher.py
│   ├── test_cleaner.py
│   ├── test_storage.py
│   ├── test_calculator.py
│   └── test_integration.py
├── .github/
│   └── workflows/
│       └── ci.yml
├── Dockerfile
├── requirements.txt
└── README.md
```

## Technologien

- Python 3.14.3
- Streamlit
- Pandas
- Pytest
- Black / Flake8
- Docker
- GitHub Actions

## Entwicklungsplan

| Sprint | Ziel |
|---|---|
| Sprint 1 | Projektstruktur & Konfiguration |
| Sprint 2 | Dashboard Mockup |
| Sprint 3 | Backend Stub-Dateien |
| Sprint 4 | Frontend Stub |
| Sprint 5 | Testdateien |
| Sprint 6 | CI/CD & Docker |
| Sprint 7 | Dokumentation & Abgabe |

## Installation

```bash
pip install -r requirements.txt
```

## Starten des Dashboards

```bash
streamlit run frontend/dashboard.py
```

---
Developed by Ibrahim Talha Sülün