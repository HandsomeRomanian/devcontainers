FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu
ARG FLUTTER_VERSION="3.3.10"

RUN apt update && apt install git && apt clean

RUN mkdir "/flutter"
RUN git clone https://github.com/flutter/flutter.git /flutter
RUN cd /flutter && git checkout ${FLUTTER_VERSION}
ENV PATH "$PATH:/flutter/bin"
RUN chown -R vscode /flutter

RUN flutter precache