FROM stingar/cowrie:1.9.1

USER root
WORKDIR /code
RUN apt-get update && apt-get install -y git build-essential
RUN git clone https://github.com/D4-project/d4-core.git
WORKDIR /code/d4-core/client
RUN git submodule init
RUN git submodule update
RUN make
RUN apt-get -y install socat
USER cowrie
