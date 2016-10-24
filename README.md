# docker-ubuntu
A base Ubuntu Docker container with en_AU (UTF8) locale support and upgraded `udev`.

The [_deboostrap_ Docker Ubuntu variant](https://hub.docker.com/_/ubuntu-debootstrap/) is used to build these images.

This image is automatically built via the Docker Hub and is available at [chinthakagodawita/ubuntu](https://hub.docker.com/r/chinthakagodawita/ubuntu/).

Its intended use is for Docker container projects that are built on CI tools (such as CircleCI) that run on LXC. These can't reconfigure locale information due to their security setups.

`udev` also can't be installed or upgraded due to [security issues on CircleCI](https://discuss.circleci.com/t/unable-to-install-udev-package-apparmor/657/2).

## Available Images

* Ubuntu 16.04
    - `chinthakagodawita/ubuntu:16.04`
    - `chinthakagodawita/ubuntu:latest`
* Ubuntu 14.04
    - `chinthakagodawita/ubuntu:14.04`
* Ubuntu 12.04
    - `chinthakagodawita/ubuntu:12.04`

## Building
```bash
docker build -t chinthakagodawita/ubuntu:16.04 16.04/
docker build -t chinthakagodawita/ubuntu:14.04 14.04/
docker build -t chinthakagodawita/ubuntu:12.04 12.04/
```
