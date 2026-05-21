# Image de base : Node.js 22 sur Alpine (légère)
FROM node:22-alpine

# Dossier de travail dans le conteneur
WORKDIR /app

# Copie des fichiers de dépendances en premier (optimisation du cache Docker)
COPY package*.json ./

# Installation des dépendances
RUN npm install --omit=dev

# Copie du reste du code source
COPY . .

# Exposition du port 3000
EXPOSE 3000

# Commande de lancement de l'API
CMD ["node", "index.js"]
