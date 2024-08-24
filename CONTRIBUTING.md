[[_TOC_]]

# How to run it

This project provides source code to bootstrap a local deployment over docker.

**Assuming you have read [README.md](README.md) and are already comfortable about what the project does and what would be the expected outcome from this project**

## Dependencies

- Docker engine
- Docker compose
- Ports: 80

## Special hardware required?

Yes, minimum system requirement

- CPU: 2 cores or more
- RAM: 8 GB or more
- Storage: 50 GB or more

## Setup and Configuration for local deployment

This source repository encapsulates various repositories as submodules. We will start by cloning the code to local machine.

```
git clone --recurse-submodules -j8 git@github.com:samueljazzjohn/NoteKeeper-Sandbox.git
```

If a new sub-module is added to Sandbox, run following commands to pull the sub-module changes from sandbox

```
git submodule update
```


After cloning the source, to start the docker services run

```
docker-compose up --build -d
```

## How to test

This project creates various services, such of which are exposed using Traefik.

To test the successful deployment visit:

- http://app.localhost for notekeeper-dashboard
- http://api.localhost for notekeeper-backend