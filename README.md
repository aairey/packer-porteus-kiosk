# packer-porteus-kiosk

Repository for building a Porteus Kiosk image using a predefined config.

Also used to build a [Vagrant Box on Atlas](https://atlas.hashicorp.com/aairey/boxes/porteus-kiosk).

## Usage

Build using VirtualBox

    packer build -only=virtualbox-iso porteus-kiosk.json

Build using VMWare:

    packer build -only=vmware-iso porteus-kiosk.json

The result will be a `.box` file which you can then use with vagrant.

    vagrant box add porteus-kiosk.box
    vagrant init porteus-kiosk
    vagrant up

## Adjusting image details

The config is loaded through HTTP.
You can change the config in `http/porteus-kiosk.cfg` to your liking.
