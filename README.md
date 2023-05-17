# Deploy-Redfish-Mockup-Server
Deploy the DMTF Redfish Mockup Server in Kubernetes with additional mockups

## About

This manifest will deploy the DMTF [Redfish-Mockup-Server](https://github.com/DMTF/Redfish-Mockup-Server "https://github.com/DMTF/Redfish-Mockup-Server") in Kubernetes, with the additional mockups added.  In addition, this deployment demonstrates how to select a different mockup than the public-rackmount1 example.

## Requirements

* This manifest deploys a LoadBalancer service using [MetalLB](https://metallb.org/ "https://metallb.org/").  Update the deployment as desired for other service types.

## Usage

```
kubectl apply -f ./deploy_redfish_mockup.yaml
```
