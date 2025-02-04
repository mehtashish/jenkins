# Use a small Linux image as the base
FROM alpine:latest  

# Set a working directory inside the container
WORKDIR /app  

# Create a script to print a message
RUN echo 'echo "Hello, Docker!"' > hello.sh  

# Make the script executable
RUN chmod +x hello.sh  

# Define the command to run the script
CMD ["/bin/sh", "hello.sh"]
