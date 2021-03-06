# VNF Asterisk

In this repository you'll end up finding a mish-mash of information around a
project that [@dougbtv](https://github.com/dougbtv) and [@leifmadsen](https://github.com/leifmadsen) are working on. For this project, we
intend to build out an Asterisk-based VNF (virtual network function).

This VNF will not be intended to be deployed to production, but rather provide
a set of reference material and examples of how you might go about building
one. You can think of this as more of a demo or research project.

More information to follow as work progresses.

# Topology

## Basic topology

Initially we'll start out with a very basic topology which will have nothing to
do with any VNF work. We'll simply use this to gather up some data and basic
configuration of Asterisk and SIPp to validate we can pass data through
Asterisk and reflect it back.

![basic_topology][basic_topology]

## Adding a controller

We'll then move into the first phase of development where our Asterisk machines
will be instantiated and configured via a controller. We'll make use of the
Asterisk REST Interface (ARI) and sorcery in order to push all configuration
information to Asterisk with very little pre-configuration.

![controlled_asterisk][controlled_asterisk]

## Creating containers

After we've got our basic topology created and controller built and working,
we'll start the process of moving to a container based infrastructure.

![container_asterisk][container_asterisk]

## Building a VNF

In the next phase we'll migrate things to Kubernetes and start making things
look a lot more like a true VNF. Components will be broken into specific
components and deployed via pods, and different networking interfaces will be
added based on what components need to communicate among each other.

![vnf_overview][vnf_overview]

[basic_topology]: images/basic_topology.png
[controlled_asterisk]: images/controlled_asterisk.png
[container_asterisk]: images/container_asterisk.png
[vnf_overview]: images/vnf_overview.png
