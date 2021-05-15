# geophone-manifests

Yocto manifest file for geophone project

# setup

    $ repo init -u git@github.com:zuckerman-dev/geophone-manifests.git -b warrior
    $ repo sync

# build

    $ source poky/oe-init-build-env build
    $ bitbake geophone-image

## build SDK

    $ bitbake geophone-image -c populate_sdk

# repo tool

    $ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo