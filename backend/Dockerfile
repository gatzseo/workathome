FROM golang:1.21-alpine

WORKDIR /app

COPY . .

# Initialize module and download dependencies if needed
RUN test -f go.mod || go mod init myapp-backend
RUN go mod tidy
RUN go build -o main .

EXPOSE 8080

CMD ["./main"]