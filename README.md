# yocto-docker

## Manually build a yocto-builder docker image
```
$ git clone https://github.com/kimd98/yocto-docker.git -b jetson-nano yocto-docker
$ docker build --no-cache --tag "gumstix2021lena/yocto:jetson-nano" yocto-docker
```

## Start the container and build a console image with default settings
  ### jetson nano
```
  $ docker run --rm -it \
   > -v ~/gumstix-image:/yocto/build/tmp/deploy/images \
   > -e MACHINE=jetson-nano-emmc \
   > -e IMAGE=gumstix-console-image \
   > -e UID=$(id -u) -e GID=$(id -g) \
   > gumstix2021lena/yocto:jetson-nano
 ```
