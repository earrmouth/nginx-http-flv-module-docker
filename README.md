<h1 align="center">nginx-http-flv-module-docker</h1>
<p align="center">
    <em>Build a Stream Server with Nginx</em>
</p>

<p align="center">
    <img src="https://custom-icon-badges.herokuapp.com/github/license/TechProber/nginx-http-flv-module-docker?logo=law&color=orange" alt="License"/>
    <img src="https://custom-icon-badges.herokuapp.com/github/workflow/status/TechProber/nginx-http-flv-module-docker/Docker%20Weekly%20Cron%20CI?logo=check-circle-fill&logoColor=white"/>
    <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FTechProber%2Fnginx-http-flv-module-docker&count_bg=%235322B2&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/>
    <img src="https://custom-icon-badges.herokuapp.com/badge/docker-v20.10-blue.svg?logo=docker&logoColor=blue" alt="Docker">
    <img src="https://custom-icon-badges.herokuapp.com/badge/registry-quay.io-red.svg?logo=package&logoColor=white" alt="Registry">
    <img src="https://custom-icon-badges.herokuapp.com/github/last-commit/TechProber/nginx-http-flv-module-docker?logo=history&logoColor=white" alt="lastcommit"/>
</p>

## Introduction

CopyRight 2021-2022 TechProber. All rights reserved.

Maintainer: [ Kevin Yu (@yqlbu) ](https://github.com/yqlbu), [ Huang (@earrmouth) ](https://github.com/earrmouth), and [ Su (@SuLingGG) ](https://github.com/SuLingGG)

This repo serves to provide the end-users a way to host their stream server easily with Nginx

##### Import Notes:

> Both `rtmp` and `http` are recognized as `stream` in Nginx

## Usage Guide

Since this repository is a clone from the original [nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module), please find the detail usage guide from it

## Preparation

Create the `/etc/nginx/` directory

```bash
sudo mkdir -p /etc/nginx
cd /etc/nginx
```

### Nginx Configuration

##### Import Notes:

> The `nginx.conf` are stored under `/etc/nginx/`, you may modify the default path to adjust your need.

Replace `./nginx.conf` with your own configuration, if you plan to add extra configurations such as `rewrite-rules`. During the container build period, The `nginx.conf` will be copied to the associated path in the container.

### Custom http assets

##### Import Notes:

> The `http-assets` are stored under `/etc/nginx/`, you may modify the default path to adjust your need.

Place your http assets under `/etc/nginx/`. The data will be mapped to `/www` inside the container

## Run Locally

```bash
# run container locally
make run

# restart container locally
make restart

# run with docker-compose natively
docker-compose up -d
```

## CN Support

Use the `cn-alicloud` as apk source to build the image locally

```bash
# run container locally
docker-compose -f ./build/cn-support/docker-compose.yml up -d

# restart container locally
docker-compose -f ./build/cn-support/docker-compose.yml up -d --force-recreate
```

## Latest Releases

- nginx - https://nginx.org/download/
- nginx-http-flv-module - https://github.com/winshining/nginx-http-flv-module/archive/refs/tags/

## References

- https://github.com/alfg/docker-nginx-rtmp/blob/master/Dockerfile
- https://github.com/nginxinc/docker-nginx/blob/6f0396c1e06837672698bc97865ffcea9dc841d5/mainline/alpine-perl/Dockerfile
- https://github.com/winshining/nginx-http-flv-module-docker/blob/master/README.CN.md
- https://www.jianshu.com/p/123df9333db0
- https://blog.csdn.net/syy014799/article/details/121885306
- https://blog.csdn.net/a_917/article/details/121473954
- https://hub.docker.com/r/mycujoo/nginx-http-flv-module-docker
- https://blog.csdn.net/a_917/article/details/121473954?spm=1001.2014.3001.5502
- https://blog.csdn.net/a_917/article/details/106709928
- https://blog.csdn.net/Prinz_Corn/article/details/120746676
- https://blog.csdn.net/xjcallen/article/details/107174374

## License

[MIT (C) TechProber](https://github.com/TechProber/nginx-http-flv-module-docker/blob/master/LICENSE)
