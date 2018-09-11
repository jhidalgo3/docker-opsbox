# Description

Docker image with installed CLI tools: `ansible`, `aws`, `kubectl`

# Versions

* Ansible  `2.4.1.0`
* AWSCLI   `1.15.59`
* Kubectl  `v1.8.5`

# Basic usage

```
docker run --rm jhidalgo3/opsbox ansible --help
docker run --rm jhidalgo3/opsbox aws help
docker run --rm jhidalgo3/opsbox kubectl --help
```

# Advanced usage

```
docker run -ti -v ${HOME}/.kube -v ${PWD}:/mnt/opsbox/.kube jhidalgo3/opsbox kubectl get po --all-namespaces
docker run -ti --rm -v ${HOME}/.aws:/mnt/opsbox/.aws jhidalgo3/opsbox aws ec2 describe-instances --region eu-west-1 --profile <PROFILE>

docker run -ti --rm -v ${HOME}/.aws:/mnt/opsbox/.aws jhidalgo3/opsbox ansible --version
```
