# **Kind - CHEAT SHEET**
![kind-logo](img/kind-logo.png)

[![Badge](https://img.shields.io/github/last-commit/jorgegabrielti/gcp-cheatsheet)](https://github.com/jorgegabrielti/gcp-cheatsheet)

About
==========
This repository is dedicated to Kubernetes projects using Kind.

[![Badge](https://img.shields.io/badge/Requirements-Docker-blue)](https://docs.docker.com/engine/install)
[![Badge](https://img.shields.io/badge/Requirements-Kubectl-blue)](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)


[//]: # "[![Badge]()]()"

Table of contents
==========
<!--ts-->
   * [About](#about)
   * [Table of contents](#table-of-contents)
   * [Requirements](#requirements)

<!--te-->

[//]: # "(## Feature)"
[//]: # "(- [x] [Packages utils](src/conf/packages.txt))"

Requirements
==========
- [x] **Docker**

---
Requirement             | How to install
-------------------------|----------------
**Docker**               | [**here**](https://docs.docker.com/engine/install/)
**Kubectl**              | [**here**](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)


## Install Kind
```bash
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64
```

```bash
chmod +x ./kind
sudo mv ./kind /usr/bin/kind
```

```bash
kind --version
```

## Create a cluster (Basic)
**Syntax:**
```bash
kind create cluster --name <CLUSTER NAME>
```

**Sample**:
```bash
kind create cluster --name kind-cluster
```

By default, Kubernetes saves context settings in the <span style="color:red">${HOME}/.kube/config</span> file. To set a different location:

```bash
CLUSTER_NAME="cluster-poc"
export KUBECONFIG="~/.kube/${CLUSTER_NAME}"
```

```bash
kind create cluster --name ${CLUSTER_NAME} --kubeconfig ${KUBECONFIG}
```
