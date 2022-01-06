# syntax = edrevo/dockerfile-plus

FROM ubuntu:focal

RUN dpkg --add-architecture i386

INCLUDE+ common/Dockerfile

RUN dpkg --add-architecture i386

RUN apt-get update && apt-get install $APT_ARGS \
    g++-9-multilib \
    wine32  \
    && rm -rf /var/lib/apt/lists/*

INCLUDE+ common/Dockerfile.finish
