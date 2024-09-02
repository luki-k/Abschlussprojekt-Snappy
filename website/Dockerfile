# Verwende das offizielle Node.js-Image als Basis
FROM node:16-alpine

# Setze das Arbeitsverzeichnis im Container
WORKDIR /app

# Kopiere die package.json und package-lock.json Dateien in das Arbeitsverzeichnis
COPY package*.json ./

# Installiere die Abhängigkeiten
RUN npm install --production

# Kopiere den restlichen Quellcode in das Arbeitsverzeichnis
COPY . .

# Baue die React-Anwendung für die Produktion (optional, wenn es ein Build-Schritt gibt)
RUN npm run build

# Exponiere den Port 3000, auf dem die Anwendung läuft
EXPOSE 3000

# Starte die Anwendung
CMD ["npm", "start"]