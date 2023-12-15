# Use an official Ubuntu base image
FROM ubuntu:latest

# Set the working directory
WORKDIR /usr/src/app

# Install any necessary dependencies
RUN apt-get update && apt-get install -y \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Copy the initialization script into the container
COPY ./scripts /usr/src/app/scripts

# Make the script executable
RUN chmod +x -R /usr/src/app/scripts

# Use the initialization script as the entrypoint
ENTRYPOINT ["/usr/src/app/scripts/init-script.sh"]

# Command to run after the initialization script
CMD ["echo", "This command runs after the init script"]