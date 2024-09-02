# Wähle ein Basis-Image, das Python enthält
FROM python:3.10-slim

# Setze das Arbeitsverzeichnis im Container
WORKDIR /app

# Kopiere die requirements.txt Datei ins Arbeitsverzeichnis
COPY requirements.txt /app/

# Installiere die Python-Abhängigkeiten
RUN pip install --no-cache-dir -r requirements.txt

# Kopiere den gesamten Code aus dem aktuellen Verzeichnis (Build-Kontext) ins Arbeitsverzeichnis
COPY . .

# Exponiere den Port, auf dem die Anwendung läuft (hier Beispiel-Port 5000)
EXPOSE 5000

# Definiere den Befehl, um die Anwendung zu starten
CMD ["python", "index.py"]
