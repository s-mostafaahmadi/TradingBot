# TradingBot

Experimenteller Trading-Bot zur Analyse von Kryptomärkten und zum Backtesting einer einfachen Strategie auf Basis gleitender Durchschnitte. Das Projekt ist ein Lern- und Research-Projekt und **kein** produktionsreifer Handelsbot – es werden keine echten Orders ausgeführt.

## Aufbau

| Datei / Ordner | Inhalt |
| --- | --- |
| `Funcations.py` | Technische Indikatoren (MACD, RSI) und Hilfsfunktionen auf Pandas-DataFrames |
| `get_signal_MovingAverage.py` | Strategie `strategy1` auf Basis gleitender Durchschnitte |
| `MarketAnalysisOnline.py` | Live-Analyse: Kursdaten von Börsen über `ccxt`, animierter Chart mit Matplotlib |
| `Offline/` | Gleicher Ablauf mit simulierten Kursen (`MarketSimulation.py`, `MarketAnalysisOffline.py`) |
| `NEXT/` | Notebooks und Experimente: Börsenanbindung, LSTM-Modelle (`LC/`), Arbitrage-Ideen (`workout/`) |
| `ProgramTest.py` | Einstiegspunkt für einen Testlauf |
| `PriceData/`, `Save/` | Zwischenspeicher für Kursdaten und Ergebnisse |
| `Document.pdf` | Projektdokumentation (Konzept, Aufbau, Ergebnisse) |

## Voraussetzungen

Python 3.10+ und:

```bash
pip install pandas numpy matplotlib ccxt
```

Für die Notebooks in `NEXT/` werden zusätzlich gängige ML-Bibliotheken (u. a. Keras/TensorFlow) benötigt.

## Start

```bash
python MarketAnalysisOnline.py          # Analyse mit Live-Kursdaten
cd Offline && python MarketAnalysisOffline.py   # Analyse mit simulierten Daten
```

## Hinweis

Die Strategie ist bewusst einfach gehalten (Moving Average + Indikatoren) und dient der Veranschaulichung von Datenaufbereitung, Signalberechnung und Visualisierung. Keine Anlageempfehlung.
