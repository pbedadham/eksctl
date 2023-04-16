# EKS Cluster Deployment with eksctl
This repository provides an example of deploying an Amazon Elastic Kubernetes Service (EKS) cluster using eksctl.

## Prerequisites
* An Amazon Web Services (AWS) account
* AWS CLI
* eksctl(installation instructions [here](https://eksctl.io/introduction/#installation))

## Steps
Clone this repository to your local machine.

Open a terminal window and navigate to the repository directory.

Edit the eksctl-demo.yaml file to include your desired cluster configuration. This file specifies the cluster name, region, node group configuration, and any add-ons.

Run the following command to create the EKS cluster:

```
eksctl create cluster -f eksctl-demo.yaml
```

This will create an EKS cluster based on the configuration specified in the eksctl-demo.yaml file.

Verify that the cluster was created successfully by running the following command:

```
kubectl get nodes
```
This will list the worker nodes in the cluster.

To delete the cluster, run the following command:
```
eksctl delete cluster -f eksctl-demo.yaml
```
This will delete the EKS cluster along with any associated resources.

### Conclusion
This example demonstrates how to deploy an EKS cluster using eksctl. You can customize the cluster configuration in the eksctl-demo.yaml file to meet your specific requirements.
