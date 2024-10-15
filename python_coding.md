# README: Hinweise zur Erstellung von Python-Skripten

## Allgemeine Hinweise

Dieser Leitfaden soll dir bei der Erstellung von Python-Skripten helfen. Es werden grundlegende Best Practices und nützliche Hinweise zur Entwicklung effizienter, gut strukturierter und leicht verständlicher Skripte vorgestellt. Beachte bitte, dass dieser Code teilweise mithilfe einer KI erstellt wurde und vom Ersteller kein professioneller Programmierer ist. Der Code kann unvollständig oder fehlerhaft sein und logische Lücken aufweisen.

## Best Practices für Python-Skripte

### 1. Verwendung einer virtuellen Umgebung

Erstelle eine virtuelle Umgebung, um die Abhängigkeiten des Projekts getrennt zu halten. Das erleichtert die Wartung und vermeidet Konflikte zwischen verschiedenen Projekten.

```bash
python -m venv venv
venv\Scripts\activate  # Windows
```

### 2. Ordnerstruktur und Dateibenennung

Strukturiere deine Dateien so, dass die Wartung des Codes einfach ist. Beispiele für eine sinnvolle Struktur:

```
project_name/
|-- src/
|   |-- main.py
|   |-- module1.py
|-- tests/
|-- requirements.txt
|-- README.md
```

Verwende sprechende Dateinamen und halte dich an die Konventionen für Module in Kleinbuchstaben.

### 3. Lesbarkeit des Codes (Code Style)

Nutze eine einheitliche Code-Formatierung. Python bietet den PEP8-Standard, der sich als Leitfaden bewährt hat. Verwende Tools wie `black` oder `flake8`, um sicherzustellen, dass der Code einheitlich und sauber formatiert ist.

### 4. Kommentare und Dokumentation

Schreibe aussagekräftige Kommentare, um die Lesbarkeit deines Codes zu erhöhen. Jeder Python-Skript sollte ein Docstring im Top-Level-File enthalten, um den Zweck zu erklären.

```python
"""
Dieses Skript dient zur Verarbeitung von Daten und zur Berechnung statistischer Metriken.
"""
```

### 5. Modularisierung

Teile deinen Code in kleinere, gut verständliche Module auf. Das erleichtert die Wiederverwendung und Testbarkeit von Funktionen und Klassen.

### 6. Type Hints verwenden

Nutze Type Hints, um den Datentypen von Funktionsparametern und Rückgabewerten anzugeben. Dies erhöht die Lesbarkeit und hilft IDEs und Tools, Fehler frühzeitig zu erkennen.

```python
def add_numbers(a: int, b: int) -> int:
    return a + b
```

### 7. Abhängigkeiten festhalten

Verwende `requirements.txt` oder `Pipfile`, um die Abhängigkeiten des Projekts zu dokumentieren. Dadurch wird sichergestellt, dass andere Entwickler oder Benutzer alle notwendigen Bibliotheken einfach installieren können.

```bash
pip freeze > requirements.txt
```

### 8. Fehlerbehandlung

Verwende try-except-Blöcke zur Fehlerbehandlung und logge Fehlermeldungen, um die Ursachen später nachzuvollziehen.

```python
try:
    # Code der ausgeführt wird
except Exception as e:
    print(f"Fehler aufgetreten: {e}")
```

### 9. Testen

Schreibe Unit-Tests, um sicherzustellen, dass der Code wie erwartet funktioniert. Verwende Frameworks wie `unittest` oder `pytest` für die Entwicklung und Ausführung der Tests.

```python
def test_function():
    assert my_function(2, 3) == 5
```

### 10. Datenverarbeitung und Ausgabe

Falls das Skript Daten ausgibt (z.B. in Form einer Excel-Datei), nutze vorzugsweise DIN 1355-1 als Formatstandard und achte darauf, dass CSV-Dateien im Encoding 'windows-1252' erstellt werden, um Probleme mit Sonderzeichen zu vermeiden.

### 11. Protokollierung (Logging)

Nutze das Modul `logging` statt `print()`, um eine konsistente und flexible Protokollierung in deinem Code zu ermöglichen.

```python
import logging
logging.basicConfig(level=logging.INFO)
logger = logging.getLogger(__name__)
logger.info("Dies ist eine Info-Nachricht")
```

### 12. Nutzung von externen Bibliotheken

Verwende Bibliotheken, die sich für bestimmte Aufgaben als nützlich erwiesen haben. Beispiele sind `pandas` und `numpy` für Datenverarbeitung, `requests` für HTTP-Anfragen oder `matplotlib` für Visualisierungen. Diese können effizient und vielfältig eingesetzt werden.

## Schlusswort

Python-Skripte können die Grundlage für verschiedenste Anwendungen darstellen. Durch die Befolgung dieser Best Practices bleibt dein Code lesbar, effizient und erweiterbar. Beachte jedoch, dass alle hier gezeigten Beispiele keine fertigen Produkte darstellen, sondern als Orientierung dienen. Lass dich davon inspirieren und experimentiere weiter!