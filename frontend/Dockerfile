# Image de base : Node.js 22 sur Alpine
FROM node:22-alpine

# Dossier de travail
WORKDIR /app

# Copie des fichiers de dépendances en premier (cache Docker)
COPY package*.json ./

# Installation de toutes les dépendances (dev incluses pour Vite)
RUN npm install

# Copie du reste des sources
COPY . .

# Exposition du port de développement Vite
EXPOSE 5173

# Lancement du serveur de développement
# --host 0.0.0.0 pour exposer Vite hors du conteneur
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
