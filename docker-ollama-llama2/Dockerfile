# This sets the base image for the Docker image. It specifies that the image will be built on top of Ubuntu 20.04.
FROM ubuntu:20.04

# This RUN instruction is used to execute commands within the image.
#It updates the package lists (using apt-get update) and installs the curl tool (using apt-get install -y curl).
#This is necessary to download files from the internet in the subsequent steps.
RUN apt-get update && apt-get install -y curl

# This RUN instruction does two things: It uses the curl command to download the Ollama binary from the specified  \
#URL (https://ollama.ai/download/ollama-linux-amd64) and saves it as /usr/bin/ollama in the Docker image.
RUN curl -L https://ollama.ai/download/ollama-linux-amd64 -o /usr/bin/ollama && \
    chmod +x /usr/bin/ollama

# This instruction sets the working directory within the image to /llama2. \
#Any subsequent commands executed within the image will be relative to this directory.
WORKDIR /llama2

# This CMD instruction specifies the default command that should be run when a container is started from the built image.
#In this case, it runs the ollama binary with the argument "serve."
CMD ["ollama", "serve"]

