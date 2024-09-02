ARG base
FROM ${base}

USER root

# Dazzle does not rebuild a layer until one of its lines are changed. Increase this counter to rebuild this layer.
ENV TRIGGER_REBUILD=2

# Install Wash CLI 
RUN curl -s https://packagecloud.io/install/repositories/wasmcloud/core/script.deb.sh |  bash \
    && apt install wash

USER gitpod

RUN wash up -d && wash down
RUN wash completions -d $HOME/.wash bash && \
  echo "\n source $HOME/.wash/wash.bash \n"\
  >> $HOME/.bashrc

EXPOSE 4222 \
       4223