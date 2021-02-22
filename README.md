# yocto-docker

## Manually build a yocto console image
```
$ git clone https://github.com/kimd98/yocto-docker.git yocto-docker
$ docker build --no-cache --tag "gumstix2021lena/yocto:latest" yocto-docker
```

## Start yocto container and build an image with default settings
  ### raspberry pi cm3
  ```
  $ docker run --rm -it \
   > -v ~/gumstix-image:/yocto/build/tmp/deploy/images \
   > -e MACHINE=raspberrypi-cm3 \
   > -e IMAGE=gumstix-console-image \
   > -e UID=$(id -u) -e GID=$(id -g) \
   > gumstix2021lena/yocto:latest
```
  
  ### jetson nano
```
  $ docker run --rm -it \
   > -v ~/gumstix-image:/yocto/build/tmp/deploy/images \
   > -e MACHINE=jetson-nano-emmc \
   > -e IMAGE=gumstix-console-image \
   > -e UID=$(id -u) -e GID=$(id -g) \
   > gumstix2021lena/yocto:latest
 ```
