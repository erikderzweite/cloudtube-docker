# Cloudtube docker
[![Docker hub - abeltramo/cloudtube](https://img.shields.io/badge/docker-abeltramo%2Fcloudtube-success)](https://hub.docker.com/repository/docker/abeltramo/cloudtube) [![Docker Image Size (latest by date)](https://img.shields.io/docker/image-size/abeltramo/cloudtube)](https://hub.docker.com/repository/docker/abeltramo/cloudtube/tags?page=1&ordering=last_updated)

[![Docker hub - abeltramo/newleaf](https://img.shields.io/badge/docker-abeltramo%2Fnewleaft-success)](https://hub.docker.com/repository/docker/abeltramo/newleaf) [![Docker Image Size (latest by date)](https://img.shields.io/docker/image-size/abeltramo/newleaf)](https://hub.docker.com/repository/docker/abeltramo/newleaf/tags?page=1&ordering=last_updated)

Github actions to build [Cloudtube](https://git.sr.ht/~cadence/cloudtube) and [NewLeaf](https://git.sr.ht/~cadence/NewLeaf) Docker containers.


## How to use

A precompiled Docker image is available for both projects, this is a multi-arch image and will run on amd64, aarch64, and armhf devices, including the Raspberry Pi.
See the instructions on how to run Cloudtube on the [official documentation](https://git.sr.ht/~cadence/tube-docs/tree/main/item/docs).

```
docker run -d \
  -p 10412:10412 \
  --name cloudtube \
  -v ~/cloudtube/db/:/workdir/db \
  -v ~/cloudtube/config.js/:/workdir/config/config.js \
  abeltramo/cloudtube:latest
```

```
docker run -d \
  -p 3000:3000 \
  --name newleaf \
  -v ~/cloudtube/configuration.py:/workdir/configuration.py \
  abeltramo/newleaf:latest
```

