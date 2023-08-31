FROM debian:latest

#Expose port 80 for HTTP
EXPOSE 80

#Install nginx and remove default settings
RUN apt-get update && \
    apt-get install nginx -y && \
    rm -rf /var/lib/apt/lists/*

#Start Nginx
CMD ["nginx", "-g", "daemon off;"]
