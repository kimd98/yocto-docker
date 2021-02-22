# yocto-docker

## raspberry pi cm3
docker run --rm -it \
  -v ~/gumstix-image:/yocto/build/tmp/deploy/images \
  -e MACHINE=raspberrypi-cm3 \
  -e IMAGE=gumstix-console-image \
  -e UID=$(id -u) -e GID=$(id -g) \
  gumstix/yocto-builder:latest
  
  ## jetson nano
  docker run --rm -it \
  -v ~/gumstix-image:/yocto/build/tmp/deploy/images \
  -e MACHINE=jetson-nano-emmc \
  -e IMAGE=gumstix-console-image \
  -e UID=$(id -u) -e GID=$(id -g) \
  gumstix/yocto-builder:latest
