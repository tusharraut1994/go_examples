# Start from golang v1.11 base image
FROM golang:1.11

# Add Maintainer Info
LABEL maintainer="Tushar Raut<tusharraut444@gmail.com>"

# Set the Current Working Directory inside the container
WORKDIR $GOPATH/src/github.com/tushar/terminal

# Copy everything from the current directory to the PWD(Present Working Directory) inside the container
COPY . .

# Download all the dependencies
RUN go get -d -v ./...

# Install the package
RUN go install -v ./...

# This container exposes port 8000 to the outside world
EXPOSE 8000

# Run the app1 main program
CMD ["go", "run", "./file_server/main.go", "--port", "8000"]