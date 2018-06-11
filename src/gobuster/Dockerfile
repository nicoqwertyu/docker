FROM debian:stretch

WORKDIR /root/

RUN apt-get update
RUN apt-get -y install dialog git golang

ENV GOPATH=/usr/share/go/
ENV PATH=/usr/lib/go/bin/:$PATH

RUN go get "github.com/OJ/gobuster"

ENTRYPOINT ["gobuster"]
CMD ["-h"]
