#### General Settings
|Key|Value|Default|Description|
|---|---|---|---| 
|appName|String|userservice|Application Name used to name the Kubernetes resources|
|environment|String|production|Environment name used for Namespace|
|replicas|Number|3|Number of POD replicas|
|prometheus|Bolean|true|Enable or Disable Prometheus annotations|

#### Secrets Settings
|Key|Value|Default|Description|
|---|---|---|---| 
|secrets:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;samplePassword:|String|abcpass|Name used to compose secret name with app name and environment|

#### Service/Ingress Settings
|Key|Value|Default|Description|
|---|---|---|---| 
|url|String|user.day.io|Host URL for application|
|port|Number|8080|TCP port for application|

#### Node Affinity Settings
|Key|Value|Default|Description|
|---|---|---|---| 
|affinity:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;key:|String|kubernetes.io/os|Key used for nodeAffinity|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;value:|String|linux|Key used for nodeAffinity|

#### Container Settings
|Key|Value|Default|Description|
|---|---|---|---| 
|docker:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registry:|String|ghcr.io|URL Base for Registry|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;image:|String|lazevedo-devops/dayio-userservice:main/|Path to the docker image|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;container:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;memoryLimits:|String|1024Mi|Limit of Memory to be used|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;memoryRequests:|String|512Mi|Request of Memory to be used|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;cpuLimits:|String|1000m|Limit of CPU to be used|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;cpuRequests:|String|500m|Request of CPU to be used|