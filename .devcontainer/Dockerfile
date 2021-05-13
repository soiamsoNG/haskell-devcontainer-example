FROM docker.io/haskell:8.10.4

COPY --chown=root:root config /root/.cabal/config
COPY --chown=root:root stack-tuna-config.yaml /root/.stack/config.yaml
COPY --chown=root:root stack-global-config.yaml /root/.stack/global-project/stack.yaml
COPY --chown=root:root sources.list /etc/apt/sources.list

RUN cabal update
# ENV LANG C.UTF-8  # docker-haskell should already make this as default
RUN apt-get -o Acquire::Check-Valid-Until=false update;
