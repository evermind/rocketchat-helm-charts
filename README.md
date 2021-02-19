# helm-chart
Future home of helm3 chart


# Develop

calling lint local with 
```
docker run -w "/data" -v ${PWD}:/data quay.io/helmpack/chart-testing:v3.3.1 ct lint --chart-repos 'bitnami=https://charts.bitnami.com/bitnami' 
```
