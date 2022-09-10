summary: ASM Multi-Cluster Lab
id: asm-mcrcp-lab
categories: cloud
tag: anthos
status: Published
authors: Vinesh
Feedback Link: https://codelabs.devnull.fyi

# 205 - ASM Multi-Cluster Replicated Control Plane

<!-- ---------------------------------------------------------------------------- -->
## Overview

Duration: 4

Follow this guide to install an Istio [multicluster deployment](https://istio.io/latest/docs/ops/deployment/deployment-models/#multiple-clusters) with replicated [control plane](https://istio.io/latest/docs/ops/deployment/deployment-models/#control-plane-models) instances in every cluster and using gateways to connect services across clusters.

Instead of using a shared Istio control plane to manage the mesh, in this configuration each cluster has its own Istio control plane installation, each managing its own endpoints.

A single Istio service mesh across the clusters is achieved by replicating shared services and namespaces and using a common root CA in all of the clusters. Cross-cluster communication occurs over the Istio gateways of the respective clusters.

<!-- ---------------------------------------------------------------------------- -->
## Add clusters to an Anthos Service Mesh

Duration: 30

### Join two clusters with Anthos Service Mesh into a single mesh

To join two clusters we will use ASM 1.6's Multi Cluster feature. This is a specific mode of multicluster Istio where two separate Kubernetes clusters run their own Istio control plane, and orchestrate their own mesh.

In this lab you will unite two clusters with Anthos Service Mesh pre-installed into one logical, hybrid mesh, by enabling cross-cluster load balancing between them. Is is possible to extend this process to incorporate any number of clusters into a single mesh.

Instructions for this activity can be found [here](https://cloud.google.com/service-mesh/docs/gke-install-multi-cluster).

### Deploy Online Boutique Application across clusters

In this activity we will orchestrate the online boutique application with Anthos Service Mesh across two different Google Kubernetes Engine clusters.

Instructions for this activity can be found [here](https://github.com/mvpzone/hipster/tree/master/mcrcp).

![Boutique Multi-Cluster Deployment](assets/hipster-mcrcp-topology.png)

<!-- ---------------------------------------------------------------------------- -->
## Having Trouble

Duration: 1

These labs are new for Q2 '20, and you may hit a roadblock or a bug. If this happens, email the labs Google Group - [hybrid-sme-labs-2020@google.com](mailto:hybrid-sme-labs-2020@google.com), and a lab owner will be in touch to help.
