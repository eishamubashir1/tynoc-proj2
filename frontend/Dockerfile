FROM nginx:alpine

# Default Nginx html contents ko remove karein
RUN rm -rf /usr/share/nginx/html/*

# Local static frontend code container mein copy karein
COPY . /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
