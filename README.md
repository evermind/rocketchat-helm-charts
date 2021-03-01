
# helm-chart
Future home of helm3 chart


# Develop

calling lint local with 
```
docker run -w "/data" -v ${PWD}:/data quay.io/helmpack/chart-testing:v3.3.1 ct lint --chart-repos 'bitnami=https://charts.bitnami.com/bitnami' 
```

# helm-charts from old repo

This is helm repository for RocketChat charts. Follow the steps below to start deploying any of them in your Kubernetes cluster.

## Usage

### Helm3

Be sure you have helm3 binary insalled, add this repository and install rocketchat chart:

```bash
$ helm repo add rocketchat https://rocketchat.github.io/helm-charts
```

```bash
$ helm install --set mongodb.mongodbUsername=rocketchat,mongodb.mongodbPassword=changeme,mongodb.mongodbDatabase=rocketchat,mongodb.mongodbRootPassword=root-changeme my-rocketchat rocketchat/rocketchat
```

### Helm2

We still support helm2, this will only work using helm2 binary and tiller deployment running in your k8s cluster:

```bash
$ helm repo add rocketchat https://rocketchat.github.io/helm-charts
```

```bash
$ helm install --set mongodb.mongodbUsername=rocketchat,mongodb.mongodbPassword=changeme,mongodb.mongodbDatabase=rocketchat,mongodb.mongodbRootPassword=root-changeme --name my-rocketchat rocketchat/rocketchat --version 3.0.0
```

