FROM debian:latest

#Install Redis
RUN apt-get update && apt-get install -y redis-server && rm -rf /var/lib/apt/lists/*

#Expose Redis default port
EXPOSE 6379

#Run Redis with the custom configuration file
CMD ["redis-server", "/etc/redis/redis.conf"]
