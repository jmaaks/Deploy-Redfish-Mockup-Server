# Deploy-Redfish-Mockup-Server
Deploy the DMTF Redfish Mockup Server in Kubernetes with additional mockups

## About

This manifest will deploy the DMTF [Redfish-Mockup-Server](https://github.com/DMTF/Redfish-Mockup-Server "https://github.com/DMTF/Redfish-Mockup-Server") in Kubernetes.

This deployment also includes the DMTF-published sample mockups linked from the repo above and demonstrates how to select a different mockup than the public-rackmount1
example. The following section of the manifest file shows how to select a particular mockup, as well as the others that are available.

```
        args: ["-D", "/mockups/public-bladed", "--short-form"]
# Available mockups include:
# public-bladed, public-catfish, public-constrained-composition, public-nvmeof-jbof, public-pmem-configuration, public-sasfabric, public-tower
# public-bladed-partitions, public-composability, public-expansion-box, public-oem-examples  public-power-shelf, public-smartnic
# public-acd, public-cables, public-compose-action, public-localstorage, public-pdu, public-rackmount1, public-telemetry

```

## Requirements

* This manifest deploys a LoadBalancer service using [MetalLB](https://metallb.org/ "https://metallb.org/").  Update the deployment as desired for other service types.

## Usage

```
kubectl apply -f ./deployRedfishMockupServer.yaml
```
