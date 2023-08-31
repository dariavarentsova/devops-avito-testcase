FROM debian:latest

#Install Go packages 
RUN apt-get update && \
    apt-get install golang-go ca-certificates -y  && \
    rm -rf /var/lib/apt/lists/*

#Set the working directory inside the container
WORKDIR /app

#Build
COPY main.go ./
RUN go mod init main && \
    go mod tidy && \
    go build -o app .

#Expose port
EXPOSE 8000

#Run
CMD ["./main"]
