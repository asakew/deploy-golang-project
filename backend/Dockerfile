# Use an official Go image
FROM golang:1.23-alpine AS builder

# Set the working directory
WORKDIR /app

# Copy go.mod and go.sum files
COPY go.mod go.sum ./

# Download Go modules
RUN go mod download

# Copy the rest of your application files
COPY . .

# Build your Go application
RUN go build -o myapp

# Use a smaller image for runtime
FROM alpine:latest

# Copy the built binary from the builder stage
COPY --from=builder /app /myapp

# Set the entry point
ENTRYPOINT ["/myapp"]
