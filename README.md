# mobilefirst-platform-8-docker-compose

> This is yet another way to run IBM Mobile First 8.0.0.0, this time as a docker container.

## Some optional configurations

Before starting, we will assume that you have Docker and docker-compose installed on your machine. The following settings can be useful:

- In the **Dockerfile** add `RUN mkdir -p /mfp/config-log4j/` to create a directory of log settings for adapters.
- In the **docker-compose.yml** file:
    - Add `./config-log4j:/mfp/config-log4j` to map adapter log setting.
    - Add `./logs:/mfp/logs` to map logs of adapters.


## Running the container

- To start: `docker-compose up -d`.
- To stop: `docker-compose down` (add `--volumes` to delete all data).

## Acknowledgment

[Ivan](https://github.com/ivanlin) - Creator of the base Docker image for this project, [ivanlin/mobilefirst
](https://hub.docker.com/r/ivanlin/mobilefirst).