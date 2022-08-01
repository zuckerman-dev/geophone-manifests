# geophone-manifests

Yocto manifest file for geophone project.

# Images

Available images.

* geophone-image

# Supported hardware

Currently supported hardware.

* Raspberry PI 3
* Raspberry PI Zero

# Setup

## Cloning sources

To clone source please use android [repo tool](https://source.android.com/setup/develop#installing-repo). At first,
run `repo init`.

    ➜  repo init -u git@github.com:zuckerman-dev/geophone-manifests.git -b dunfell

Then run `repo sync` to download latest version on sources.

    ➜  repo sync

## Building image

To build `geophone-image`, at first, init bitbake environment.

    ➜  source geophone/oe-init-build-env build

Copy default configuration to the build directory.

    ➜  cp geophone/meta-geophone/conf/local.conf.sample build/conf/local.conf
    ➜  cp geophone/meta-geophone/conf/bblayers.conf.sample build/conf/bblayers.conf

To build the main image

    ➜  bitbake geophone-image

## Building SDK

### Standard yocto sdk

To build standard SDK for `geophone-image`.

    ➜  bitbake geophone-image -c populate_sdk

The result SDK can be found in the folder `build/deploy/sdks/`. To use SDK you can read yocto guide [sdk-using-the-standard-sdk](https://docs.yoctoproject.org/2.1/sdk-manual/sdk-manual.html#sdk-using-the-standard-sdk)

### Extensible yocto sdk

To build extensible yocto SDK for `geophone-image`.

    ➜  bitbake geophone-image -c populate_sdk_ext

The result SDK can be found in the folder `build/deploy/sdks/`. To use SDK you can read yocto guide [sdk-using-the-standard-sdk](https://docs.yoctoproject.org/2.1/sdk-manual/sdk-manual.html#sdk-extensible)

# Links

* https://docs.yoctoproject.org/index.html
