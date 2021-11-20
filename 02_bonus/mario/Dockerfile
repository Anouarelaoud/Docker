FROM nginx:latest

COPY index.html /usr/share/nginx/html
COPY js/ /usr/share/nginx/html/js/
COPY sounds/ /usr/share/nginx/html/sounds/
COPY sprites/ /usr/share/nginx/html/sprites/
COPY css/ /usr/share/nginx/html/css/

EXPOSE 80

#docker build -t mario .
#docker run -d -p 8080:80 mario
