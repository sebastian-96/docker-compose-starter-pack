# Use an official Ubuntu base image
FROM ubuntu:latest

# Set the working directory
WORKDIR /usr/src/app

# Install any necessary dependencies
RUN apt-get update && apt-get install -y \
    curl \
    && rm -rf /var/lib/apt/lists/*

# The script will be mounted from the host, so no need to COPY
