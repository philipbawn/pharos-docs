# How Does Kontena Pharos Compare to Others?

- [Managed Kubernetes Solutions](#managed-kubernetes-solutions)
- [Rancher 2.0](#rancher-20)
- [Red Hat OpenShift Container Platform](#red-hat-openshift-container-platform)

## Managed Kubernetes Solutions

Managed Kubernetes Services such as [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine/), [Amazon Elastic Container Service for Kubernetes (EKS)](https://aws.amazon.com/eks/) and [Azure Container Service (AKS)](https://azure.microsoft.com/en-us/services/container-service/) offer Kubernetes-as-a-Service (should we dare to call it KaaS? :)). The cloud provider is hosting a pre-configured Kubernetes infrastructure for you. These solutions promise simplicity, peace of mind and built-in integrations to the underlying cloud infrastructure. In essence, these solutions are Kubernetes distributions tailored to work smoothly on the selected cloud provider's infrastructure.

While most of the managed Kubernetes solutions available today are not yet production grade, they might be great solutions for those who have decided to go all-in with their selected cloud provider. Very much like with managed databases, managed Kubernetes is a beautiful solution if:

* Using public cloud is not a problem
* Having increased lock-in to your cloud provider is not a problem
* Having decreased control over the underlying system is not an issue
* It works and makes your life easier; allowing you to focus on stuff that matters
* It's certified and up-to-date

If you feel a managed Kubernetes solution from one of the cloud providers is mature enough for you to use and don't have issues with managed services in general, we highly recommend using it over any "self managed" Kubernetes solution. If you have any concerns related to using managed Kubernetes, Kontena Pharos might be the ideal solution for you and you should try it out!

## Rancher 2.0

In essence, [Rancher 2.0](https://rancher.com/) is a high level concept that contains 2 main ingredients: a management tool for managing Kubernetes clusters and Rancher Kubernetes Engine (RKE) installer. They highly complement each other but may be also used as stand-alone solutions.

The Rancher management tool is designed for businesses who want to manage multiple Kubernetes clusters from a single tool. It works with RKE and any other Kubernetes setup (including Kontena Pharos). To support multi-cluster role based access control (RBAC), the cluster management tool will utilize a novel solution: it will install a proxy server that sits in front of Kubernetes API and will enforce RBAC policies before passing the requests forward to Kubernetes API. If you consider running multiple Kontena Pharos clusters, we highly recommend checking out the Rancher management tool!

According to Rancher, RKE is an extremely simple, lightning fast Kubernetes installer that works everywhere. Since RKE is just an installer, it does not have life cycle management for distro upgrades that you can find from Kontena Pharos and most of the other Kubernetes distributions. Instead, just like many other installers, it has limited functionality for upgrading individual Kubernetes components to new version. In addition, you are limited to x86 architecture and docker as your container runtime. With Kontena Pharos you can choose between docker and CRI-O runtimes, and x86 and arm64 architectures.

## Red Hat OpenShift Container Platform

Red Hat claims [OpenShift](https://www.openshift.com/container-platform/) as the industry’s most secure and comprehensive enterprise-grade container platform based on industry standards, Docker and Kubernetes. In reality, OpenShift is an enterprise PaaS solution built on Kubernetes. It is a viable solution mostly for those who value Red Hat ecosystem and enterprise offerings.

Since OpenShift is heavily influenced by PaaS abstractions, the underlying Kubernetes is not so easily accessible. It is probably the best enterprise grade PaaS solution out there and if you don’t plan to use pure Kubernetes, it is a valid option.

In addition, OpenShift offers enhanced multi-tenant capabilities that can support multiple applications, teams and deployment processes compared to pure Kubernetes distributions. While it is possible to do a similar kind of multi-tenancy with pure Kubernetes distributions, it requires additional configuration and work.
