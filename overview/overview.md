# Overview

## Table of Contents
- [About](#about)
- [Getting Started](#getting-started)
    -   [Regions](#regions)
    -   [Zones](#zones)
    -   [Compute Engine](#compute-engine)
    -   [Instance Group](#instance-group)
    -   [Cloud Load Balancing](#cloud-load-balancing)
-   [Back to Menu](../README.md/#all-about-gcp)

## About
Course will cover the key elements on GCP.

## Getting Started
### Regions
- Specific geographical location to host your resources
- Advantages
    - High Availability
    -   Low Latency
    -   Global Footprint
    -   Adhere to government regulations
### Zones
- Increased availability and fault tolerance within same region
- Each Zone has one or more discrete clusters
- Clusters are distinct physical infrastructure that is housed in a data center
- Zones in a region are connected through low-latency links
### Compute Engine
- Create and manage lifecycle of Virtual Machine (VM) instances
- Load balancing and auto-scaling for multiple VM instances
- Attach storage (& network storage) to your VM instances
- Manage network connectivity and configuration for your VM instances
- Compute Engine Machine Family
    -  **General Purpose (E2, N2, N2D, N1)** : Best price-performance ratio
        - Web and application servers, Small-medium databases, Dev environments
    -  **Memory Optimized (M2, M1)**: Ultra high memory workloads
        -  Large in-memory databases and In-memory analytics
    -  **Compute Optimized (C2)**: Compute intensive workloads
        -  Gaming applications
           <img width="1184" alt="image" src="https://github.com/inbox-pj/all-about-gcp/assets/53929164/bb59cc1a-0702-40d0-b46f-540a60ec2a5e">
- VM instance setup approach
    - Startup Script
    - Instance Template
    - Custom Image

### Instance Group
- Group of VM instances managed as a single entity
- Types of Instance Groups
  - Managed
    - Identical VMs created using a template
    - Auto-scaling, auto healing, load balancing and managed releases
    - Supports Rolling updates and Canary Deployment
    - Instance Template is mandatory to create MIG
    - Configure auto-scaling to automatically adjust number of instances based on load:
      - _Minimum_ number of instances
      - _Maximum_ number of instances
      - _Matrices_:
        - cool-down period - How long to wait before looking at auto-scaling metrics again?
        - Scale in Controls - Prevent a sudden drop in no of VM instances
  - Unmanaged


### Cloud Load Balancing
- Client to Load Balancer - HTTPS
- Load Balancer to VM instance - HTTP/HTTPS
- SSL/TLS Termination/Offloading
  - Client to Load Balancer: HTTPS/TLS
  - Load Balancer to VM instance: HTTP/TCP
- Choosing Load Balancer
<img width="1144" alt="image" src="https://github.com/inbox-pj/all-about-gcp/assets/53929164/14c374f1-c606-48d6-8d67-b5bce4c6aea6">

- Features
<img width="906" alt="image" src="https://github.com/inbox-pj/all-about-gcp/assets/53929164/db9d4146-d83a-41e7-b098-5b1f786e5211">
