# Helm Chart for User Service App

This Helm Chart contains all required items for deploy User Service App at Kubernetes Cluster.

#### Pre-Requisites

* Kubectl Installed
* Helm 3 Installed
* Kubernetes Cluster

#### Items Deployed

```Deployment```<br>
Informations regarding the application run as container, your settings, specifications, hardware requests and limits, replicas, environment variables, labels, which image uses and etc.

```Service```<br>
Configurations to expose the application thorugh Kubernetes Service..

```Secret```<br>
A Sample secret to demonstrate the usage of Environment Variables from Secret, should contain sensitive data.

```Ingress```<br>
The configuration to expose externally the Services thorugh Nginx Inggress Controller.

#### Environments

We have 2 values files for each environment, named as development.yaml and production.yaml

```development```<br>
The settins configured here is the minimun set for run the application using low hardware settings and no monitoring stack.

[See all development values description](docs/dev-values.md)

```production```
The settins configured here is the recommended set for run the application as production mode, more hardware power, replicas and ready to be monitored by Prometheus Stack.

[See all production values description](docs/prod-values.md)

#### Usage

```Install```
```code
helm upgrade --install --atomic dayio-userservice --namespace <ENVIRONMENT> --create-namespace -f <ENVIRONMENT>.yaml .
```

You'll see a message informing that Helm Release doesn't exist yet and installing after that.

#### Verifying Installation

You could use the Helm List command for see the release installed on the appropriate environment:

```code
helm -n <ENVIRONMENT> list
```

Or you could simply go the namespace and check the items deployed:

```code
kubectl -n <ENVIRONMENT> get all
```

You should be able to see the items deployed as described at the first section of this document.

#### Questions and Feedback?

Find me on the Linkedin as lazevedo-devops or feel free to contact me through mail lazevedo@darkscreen.io.