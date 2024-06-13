# Use the official Ruby image from the Docker Hub
FROM ruby:3.1

# Set environment variables
ENV LANG=C.UTF-8 \
    LC_ALL=C.UTF-8

# Install dependencies
RUN apt-get update && apt-get install -y \
  build-essential \
  libffi-dev \
  nodejs

# Create a non-root user
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && apt-get update \
    && apt-get install -y sudo \
    && echo $USERNAME ALL=\(ALL\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Switch to non-root user
USER $USERNAME

# Set the working directory
WORKDIR /workspace

# Install Jekyll and Bundler
RUN gem install jekyll bundler

# Expose the port Jekyll runs on
EXPOSE 4000
