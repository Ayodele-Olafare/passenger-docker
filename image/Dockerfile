# syntax=docker/dockerfile:1.2
FROM phusion/baseimage:jammy-1.0.4
MAINTAINER Phusion <info@phusion.nl>

ADD . /pd_build

ARG ARCH
RUN --mount=type=cache,target=/build_cache \
    rm -rf "/build_cache/${ARCH}/*" && \
    nice -n 10 /pd_build/install_base.sh && \
    rm -rf /pd_build



