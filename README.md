# Red Hat OpenShift AI Full Deploy

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

[Live build status](https://validatedpatterns.io/ci/?pattern=mcgitops)

## Start Here - WIP

If you've followed a link to this repository, but are not really sure what it contains
or how to use it, head over to [Multicloud GitOps](https://validatedpatterns.io/patterns/multicloud-gitops/)
for additional context and installation instructions

## Rationale

The goal for this pattern is to provide a blueprint to deploy Red Hat OpenShift AI on a blank cluster.

## Used products

* Red Hat OpenShift GitOps
* Red Hat Advanced Cluster Management (remove?)
* Red Hat OpenShift AI
* Red Hat OpenShift Serverless (knative)
* Red Hat OpenShift Service Mesh (istio)
* Red Hat OpenShift Pipelines (tekton)
* Node Feature Discovery Operator
* NVIDIA GPU Operator
* Hashicorp Vault (community)

## Get Started

To deploy the pattern, run ```./pattern.sh make install```. The command will run a podman image which contains all the required tools in order to deploy the pattern, such as
* ```make```
* ```helm```
* ```ansible```
After the command is issued Red Hat OpenShift GitOps is going to be installed, and after that an ArgoCD Application is going to take over and deploy this repositories' components stated in the ```values-hub.yaml``` file.