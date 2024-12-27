# Base image with dependencies
FROM debian:bullseye

# Install required packages
RUN apt-get update && apt-get install -y \
    curl \
    git \
    make \
    python3 \
    g++ \
    && apt-get clean

# Install Bun
RUN curl -fsSL https://bun.sh/install | bash
ENV PATH="/root/.bun/bin:$PATH"

# Set up font builder
WORKDIR /work
