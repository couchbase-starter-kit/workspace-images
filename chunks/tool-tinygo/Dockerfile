ARG base
FROM ${base}

USER root

# Dazzle does not rebuild a layer until one of its lines are changed. Increase this counter to rebuild this layer.
ENV TRIGGER_REBUILD=2

# Install TinyGo 
RUN wget https://github.com/tinygo-org/tinygo/releases/download/v0.34.0/tinygo_0.34.0_amd64.deb && dpkg -i tinygo_0.34.0_amd64.deb


USER gitpod