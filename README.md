# packer-atlas-example

[![Circle CI](https://circleci.com/gh/StefanScherer/packer-atlas-example.svg?style=svg)](https://circleci.com/gh/StefanScherer/packer-atlas-example)

This is an example to build a Vagrant Box with Packer in Atlas.
See more details in [my blog post](https://stefanscherer.github.io/automate-building-vagrant-boxes-with-atlas/).

The automated build is triggered by a WebHook in GitHub to start a build in CircleCI
that triggers a build in Atlas with `packer push`.

## Packer template

See the `ubuntu1404.json` with the post-processors section with all details about
deploying the Vagrant Box to Atlas.

## circle.yml
See the `circle.yml` for details how the glue works. It just installs packer 0.8.1
and starts the `packer push`.

## Acknowledgements

The Packer template and provision scripts are based on box-cutter/ubuntu-vm.
Check out the more up to date version at [github.com/boxcutter](https://github.com/boxcutter).
