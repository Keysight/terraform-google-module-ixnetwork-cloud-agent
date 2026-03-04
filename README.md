# module-ixnetwork-cloud-agent/google

## Description
Terraform module for IxNetwork Cloud agent deployment on Google Cloud Platform

## Deployment
This module creates a single instance having three network interfaces.

## Usage
```tf
module "Agent" {
	source = "git::https://github.com/Keysight/terraform-google-module-ixnetwork-cloud-agent.git"
	Eth0SubnetName = module.Vpc.PublicSubnet.name
	Eth0VpcNetworkName = module.Vpc.PublicVpcNetwork.name
	Eth1SubnetName = module.Vpc.Private1Subnet.name
	Eth1VpcNetworkName = module.Vpc.Private1VpcNetwork.name
	Eth2SubnetName = module.Vpc.Private2Subnet.name
	Eth2VpcNetworkName = module.Vpc.Private2VpcNetwork.name
}
```
