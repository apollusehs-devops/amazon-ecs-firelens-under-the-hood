# Start from the latest golang base image
FROM golang:latest
ENV GOPROXY=direct

# Set the Current Working Directory inside the container
WORKDIR /app

# Copy the source from the current directory to the Working Directory inside the container
COPY . .

# Download all dependencies. Dependencies will be cached if the go.mod and go.sum files are not changed
RUN go mod download

# Build the Go app
RUN go build -o validator .

# Command to run the executable
CMD ["./validator"]
