FROM nginx:latest

# Cria pasta dentro do container e deixa vc dentro da pasta
WORKDIR /app

RUN apt-get update && \
    apt-get install vim -y

COPY html /usr/share/nginx/html