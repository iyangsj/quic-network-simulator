FROM ubuntu:23.04

RUN apt-get update && \
  apt-get install -y wget net-tools iputils-ping tcpdump ethtool iperf iproute2

COPY setup.sh .
RUN chmod +x setup.sh

COPY run_endpoint.sh .
RUN chmod +x run_endpoint.sh

COPY wait-for-it.sh .
RUN chmod +x wait-for-it.sh

ENTRYPOINT [ "/run_endpoint.sh" ]
