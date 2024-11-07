# Usa una versión más reciente y ligera de Node
FROM node:18-alpine

WORKDIR /usr/src/app

# Instala dependencias antes de copiar la aplicación
COPY package.json package-lock.json ./
RUN npm install --production

COPY . .

EXPOSE 8080
CMD ["npm", "start"]

# Configura el healthcheck en el docker-compose.yml para mayor flexibilidad
