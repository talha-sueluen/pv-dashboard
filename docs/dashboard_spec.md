# Dashboard Spezifikation – PV-Dashboard

## Übersicht

Das Dashboard visualisiert aktuelle und tagesbasierte Photovoltaik-Daten.
Die Daten werden aus einer externen URL abgerufen und aufbereitet angezeigt.

---

## Metriken & Visualisierungen

| Metrik | Einheit | Typ | Visualisierung |
|---|---|---|---|
| Leistung | W | Anlässlich | KPI-Karte |
| Strom | A | Anlässlich | KPI-Karte |
| Tagesertrag | kWh | Täglich | Liniendiagramm |
| Wirkungsgrad | % | Allgemein | Gauge |
| CO₂-Einsparung | kg | Allgemein | KPI-Karte |

---

## Beschreibung der Metriken

### Leistung (W)
Gibt die momentan erzeugte elektrische Leistung der PV-Anlage in Watt an.

### Strom (A)
Gibt den momentan fließenden elektrischen Strom in Ampere an.

### Tagesertrag (kWh)
Zeigt die gesamte erzeugte Energiemenge des aktuellen Tages in Kilowattstunden.
Wird als Liniendiagramm über den Tagesverlauf dargestellt.

### Wirkungsgrad (%)
Gibt an, wie effizient die PV-Anlage aktuell arbeitet.
Wird als Gauge-Diagramm dargestellt (0–100 %).

### CO₂-Einsparung (kg)
Zeigt die eingesparte CO₂-Menge basierend auf dem Tagesertrag.

---

## Mock-Daten

```python
MOCK_PV_DATA = {
    "leistung_w": 3500,
    "strom_a": 72.6,
    "tagesertrag_kwh": 18.4,
    "wirkungsgrad_pct": 75.0,
    "co2_einsparung_kg": 2.4,
    "timestamp": "2024-05-22T12:00:00"
}
```

---

## Dashboard-Layout

```
+------------------+------------------+------------------+
|   Leistung       |   Strom          |  CO₂-Einsparung  |
|   3.500 W        |   72,6 A         |   2,4 kg         |
+------------------+------------------+------------------+
|                                     |                  |
|        Tagesertrag (Linie)          |  Wirkungsgrad    |
|                                     |   (Gauge)        |
+-------------------------------------+------------------+
```

## Stub-Funktionen

| Funktion | Modul | Beschreibung |
|---|---|---|
| `fetch_pv_data()` | `fetcher.py` | Gibt Mock-PV-Daten zurück |
| `clean_data()` | `cleaner.py` | Bereinigt und validiert die Rohdaten |
| `save_data()` | `storage.py` | Speichert die bereinigten Daten als pd.DataFrame|
| `calculate_metrics()` | `calculator.py` | Berechnet Wirkungsgrad und CO₂-Einsparung |
| `show_dashboard()` | `dashboard.py` | Visualisiert die Daten mit Streamlit |