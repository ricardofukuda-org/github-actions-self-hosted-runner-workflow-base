FROM ubuntu:25.10

WORKDIR /
RUN apt update
RUN apt install -y curl zip
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
RUN unzip -q awscliv2.zip
RUN ./aws/install

COPY entrypoint.sh /entrypoint.sh
RUN chmod 700 /entrypoint.sh

ENTRYPOINT ['/entrypoint.sh']