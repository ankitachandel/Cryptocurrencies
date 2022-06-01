FROM ubuntu:16.04
LABEL maintainer  Ankita <ankitachnadel11@gmail.com>
RUN apt-get update
RUN apt-get install --yes software-properties-common
RUN add-apt-repository --yes ppa:bitcoin/bitcoin
RUN apt-get update

# install bitcoind (from PPA) and make
RUN apt-get install --yes bitcoind
ADD . /home/bitcoind-testnet
    
# WORKDIR sets the working directory for any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow
WORKDIR /home/bitcoind-testnet
EXPOSE 12001
CMD ["/bin/bash"]
