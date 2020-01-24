# Dockerized Errbit Image

Image for running [Errbit](https://github.com/errbit/errbit) in a docker container.

## NOTE

This repo is no longer being maintained. Users are welcome to fork it, but we make no warranty of its functionality.

## Usage

Errbit requires a MongoDB instance for persisting data. The Errbit container must
be linked to the MongoDB container with `mongodb` as an alias.

    docker run -d --name mongodb mongo
    docker run -d --name errbit --link mongodb:mongodb \
      -p 3000:3000 \
      centurylinklabs/errbit:0.3.0-dev
