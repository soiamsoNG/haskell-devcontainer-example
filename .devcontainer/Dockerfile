FROM haskell:8.8.4

COPY --chown=root:root config /root/.cabal/config
COPY --chown=root:root stack-tuna-config.yaml /root/.stack/config.yaml
COPY --chown=root:root stack-global-config.yaml /root/.stack/global-project/stack.yaml
COPY --chown=root:root sources.list /etc/apt/sources.list

RUN cabal update

