# Last modified: Sun, 12 Jan 2020 23:13:58 +0000
FROM mcr.microsoft.com/powershell:6.2.4-debian-stretch-slim

RUN echo 'deb http://deb.debian.org/debian buster-backports main' >> /etc/apt/sources.list

# Basic linux utilities
RUN apt-get update && apt-get install -y --no-install-recommends \
  procps \
&& rm -rf /var/lib/apt/lists/*

# Upgrade all packages to latest
RUN apt-get update && apt-get -y --no-install-recommends upgrade \
&& rm -rf /var/lib/apt/lists/*

# Upgrade using backports
RUN apt-get update && apt-get -t buster-backports -y --no-install-recommends upgrade \
&& rm -rf /var/lib/apt/lists/*

RUN groupadd --gid 4000 demisto \
  && useradd --uid 4000 --gid demisto --shell /bin/bash --create-home demisto
