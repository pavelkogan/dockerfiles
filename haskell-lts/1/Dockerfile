FROM haskell:7.8

RUN cabal update

WORKDIR /root/.cabal/
ADD http://www.stackage.org/lts/1/cabal.config?global=true lts-constraints
RUN cd /root/.cabal/ && cat lts-constraints >> config

RUN cabal update
RUN cabal install base-prelude basic-prelude
