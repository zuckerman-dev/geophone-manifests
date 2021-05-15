# geophone-manifests

Yocto manifest file for geophone project. 

# hardware

Currently supported hardware

* Raspberry PI 3 
* Raspberry PI Zero

# setup

    ➜  repo init -u git@github.com:zuckerman-dev/geophone-manifests.git -b warrior
    ➜  repo sync

# build


Init bitbake environment.

    ➜  source geophone/oe-init-build-env build

Copy default configuration to the build directory

    ➜  cp ../geophone/meta-geophone/conf/local.conf.sample conf/local.conf
    ➜  cp ../geophone/meta-geophone/conf/bblayers.conf.sample conf/bblayers.conf

To build the main image

    ➜  bitbake geophone-image

## build SDK

To build SDK for `geophone-image`

    ➜  bitbake geophone-image -c populate_sdk

# repo tool

    ➜  curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo