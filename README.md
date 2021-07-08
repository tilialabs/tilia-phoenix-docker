# tilia-phoenix-docker
Docker files for building and running headless tilia Phoenix docker containers

<a name="prerequisites"></a>
## Prerequisites

- Valid tilia Cloud license of tilia Phoenix including the Automate module
- tilia Phoenix Linux installer (deb) from [downloads.tilialabs.com](https://downloads.tilialabs.com)
- Docker container runtime environment such as Docker Desktop, Docker Swarm, or Kubernetes

## Support

Docker images of tilia Phoenix are not officially supported by Tilia Labs.  Please contact us if you have services or support needs.

## Images

### Ubuntu 20.04

This docker file uses Ubuntu 20.04 as the base image.  Ubuntu 20.04 is our officially supported Linux distro/version for Phoenix, so we generally recommend using this docker file to build your tilia Phoenix docker images.

### Debian Buster Slim

This docker file uses Debian Buster Slim as the base image, which is roughly 50MB smaller than Ubuntu 20.04, clocking in at around 500MB installed container size vs. 550MB for Ubuntu 20.04.

### Bitnami Minideb Buster

This docker file uses Bitnami's Minideb image as the base, which has a very similar install size as the Debian Buster Slim flavor above.

## Open source

All code herein is open sourced under the Apache 2.0 license.  You are free to customize and use your modifications for commercial purposes with or without publishing your changes.

Tilia Labs is the sole maintainer of this repository, but we encourage suggestions and pull requests to help make this client better than ever for our global graphic arts community!

<a name="license"></a>
## License
Copyright (c) 2021-* Tilia Labs Inc.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
