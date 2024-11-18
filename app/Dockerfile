# Etapa 1: Construcción
FROM node:18 as builder
WORKDIR /app
COPY package.json postcss.config.js tailwind.config.js ./
RUN npm install
COPY src ./src
COPY public ./public
RUN npm run build

# Etapa 2: Servir con Nginx
FROM nginx:alpine
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
