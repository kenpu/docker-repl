FROM clojure

RUN apt-get update
RUN apt-get install rlwrap

RUN mkdir /clojure
WORKDIR /clojure
RUN lein new ./bootstrap
RUN cd ./bootstrap; lein deps
WORKDIR /clojure
COPY ./clj /usr/bin
CMD /usr/bin/clj
