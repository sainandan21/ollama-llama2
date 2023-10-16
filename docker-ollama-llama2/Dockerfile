## Use an Alpine Linux base image
#FROM ubuntu:22.04
#
## Install CURL
#RUN apk add --no-cache curl
#
## Download the Ollama binary and make it executable
#RUN curl -L https://ollama.ai/download/ollama-linux-amd64 -o /usr/bin/ollama
#
## Make the Ollama binary executable
#RUN chmod +x /usr/bin/ollama
#
## Set the working directory
#WORKDIR /llama2
#
## Start Ollama
#CMD ["ollama", "serve"]

# Use Ubuntu 20.04 as the base image
FROM ubuntu:20.04

# Update package lists and install CURL
RUN apt-get update && apt-get install -y curl

# Download the Ollama binary and make it executable
RUN curl -L https://ollama.ai/download/ollama-linux-amd64 -o /usr/bin/ollama && \
    chmod +x /usr/bin/ollama

# Set the working directory
WORKDIR /llama2

# Start Ollama
CMD ["ollama", "serve"]

