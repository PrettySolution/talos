---
title: 'machined'
---

A common theme throughout the design of Talos is minimalism.
We believe strongly in the UNIX philosophy that each program should do one job well.
The `init` included in Talos is one example of this, and we are calling it "`machined`".

We wanted to create a focused `init` that had one job - run Kubernetes.
To that extent, `machined` is relatively static in that it does not allow for arbitrary user defined services.
Only the services necessary to run Kubernetes and manage the node are available.
This includes:

- [containerd](/docs/components/containerd)
- [kubeadm](/docs/components/kubeadm)
- [kubelet](https://kubernetes.io/docs/concepts/overview/components/)
- [networkd](/docs/components/networkd)
- [ntpd](/docs/components/ntpd)
- [osd](/docs/components/osd)
- [trustd](/docs/components/trustd)
- [udevd](/docs/components/udevd)
