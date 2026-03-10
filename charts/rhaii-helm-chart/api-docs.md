# rhaii-helm-chart

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.4.0-ea.2](https://img.shields.io/badge/AppVersion-3.4.0--ea.2-informational?style=flat-square)

Red Hat OpenShift AI Operator Helm chart (non-OLM installation)

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| azure | object | `{"cloudManager":{"image":"quay.io/opendatahub/opendatahub-operator:latest","imagePullPolicy":"Always","namespace":"rhai-cloudmanager-system"},"enabled":false,"kubernetesEngine":{"enabled":true,"spec":{"dependencies":{"certManager":{"configuration":{},"managementPolicy":"Managed"},"gatewayAPI":{"configuration":{},"managementPolicy":"Managed"},"lws":{"configuration":{},"managementPolicy":"Managed"},"sailOperator":{"configuration":{},"managementPolicy":"Managed"}}}}}` | Azure cloud configuration |
| azure.cloudManager | object | `{"image":"quay.io/opendatahub/opendatahub-operator:latest","imagePullPolicy":"Always","namespace":"rhai-cloudmanager-system"}` | Azure Cloud Manager configuration |
| azure.cloudManager.image | string | `"quay.io/opendatahub/opendatahub-operator:latest"` | Cloud Manager container image |
| azure.cloudManager.imagePullPolicy | string | `"Always"` | Image pull policy |
| azure.cloudManager.namespace | string | `"rhai-cloudmanager-system"` | Cloud Manager operator namespace |
| azure.enabled | bool | `false` | Enable Azure cloud support |
| azure.kubernetesEngine | object | `{"enabled":true,"spec":{"dependencies":{"certManager":{"configuration":{},"managementPolicy":"Managed"},"gatewayAPI":{"configuration":{},"managementPolicy":"Managed"},"lws":{"configuration":{},"managementPolicy":"Managed"},"sailOperator":{"configuration":{},"managementPolicy":"Managed"}}}}` | Azure Kubernetes Engine configuration |
| azure.kubernetesEngine.enabled | bool | `true` | Create AzureKubernetesEngine CR via post-install hook |
| azure.kubernetesEngine.spec | object | `{"dependencies":{"certManager":{"configuration":{},"managementPolicy":"Managed"},"gatewayAPI":{"configuration":{},"managementPolicy":"Managed"},"lws":{"configuration":{},"managementPolicy":"Managed"},"sailOperator":{"configuration":{},"managementPolicy":"Managed"}}}` | AzureKubernetesEngine CR spec |
| components | object | `{"kserve":{"enabled":true,"spec":{}}}` | Components configuration |
| components.kserve | object | `{"enabled":true,"spec":{}}` | KServe component |
| components.kserve.enabled | bool | `true` | Create Kserve CR via post-install hook |
| components.kserve.spec | object | `{}` | Kserve CR spec |
| coreweave | object | `{"cloudManager":{"image":"quay.io/opendatahub/opendatahub-operator:latest","imagePullPolicy":"Always","namespace":"rhai-cloudmanager-system"},"enabled":false,"kubernetesEngine":{"enabled":true,"spec":{"dependencies":{"certManager":{"configuration":{},"managementPolicy":"Managed"},"gatewayAPI":{"configuration":{},"managementPolicy":"Managed"},"lws":{"configuration":{},"managementPolicy":"Managed"},"sailOperator":{"configuration":{},"managementPolicy":"Managed"}}}}}` | CoreWeave cloud configuration |
| coreweave.cloudManager | object | `{"image":"quay.io/opendatahub/opendatahub-operator:latest","imagePullPolicy":"Always","namespace":"rhai-cloudmanager-system"}` | CoreWeave Cloud Manager configuration |
| coreweave.cloudManager.image | string | `"quay.io/opendatahub/opendatahub-operator:latest"` | Cloud Manager container image |
| coreweave.cloudManager.imagePullPolicy | string | `"Always"` | Image pull policy |
| coreweave.cloudManager.namespace | string | `"rhai-cloudmanager-system"` | Cloud Manager operator namespace |
| coreweave.enabled | bool | `false` | Enable CoreWeave cloud support |
| coreweave.kubernetesEngine | object | `{"enabled":true,"spec":{"dependencies":{"certManager":{"configuration":{},"managementPolicy":"Managed"},"gatewayAPI":{"configuration":{},"managementPolicy":"Managed"},"lws":{"configuration":{},"managementPolicy":"Managed"},"sailOperator":{"configuration":{},"managementPolicy":"Managed"}}}}` | CoreWeave Kubernetes Engine configuration |
| coreweave.kubernetesEngine.enabled | bool | `true` | Create CoreWeaveKubernetesEngine CR via post-install hook |
| coreweave.kubernetesEngine.spec | object | `{"dependencies":{"certManager":{"configuration":{},"managementPolicy":"Managed"},"gatewayAPI":{"configuration":{},"managementPolicy":"Managed"},"lws":{"configuration":{},"managementPolicy":"Managed"},"sailOperator":{"configuration":{},"managementPolicy":"Managed"}}}` | CoreWeaveKubernetesEngine CR spec |
| enabled | bool | `true` | Enable/disable all resource creation |
| imagePullSecret | object | `{"dependencyNamespaces":["cert-manager-operator","cert-manager","openshift-lws-operator","istio-system"],"dockerConfigJson":"","name":"rhaii-pull-secret"}` | Pull secret for private registries Use --set-file imagePullSecret.dockerConfigJson=path/to/auth.json |
| imagePullSecret.dependencyNamespaces | list | `["cert-manager-operator","cert-manager","openshift-lws-operator","istio-system"]` | Namespaces created by dependency operators where pull secrets should be injected |
| imagePullSecret.name | string | `"rhaii-pull-secret"` | Name of the pull secret to create in target namespaces. This name MUST not be changed as it is referred also in other installed dependencies and not yet configurable. |
| installCRDs | bool | `true` | Install CRDs or not using the chart |
| labels | object | `{}` | Common labels applied to all resources |
| rhaiOperator | object | `{"applicationsNamespace":"redhat-ods-applications","image":"quay.io/opendatahub/opendatahub-operator:latest","imagePullPolicy":"Always","namespace":"redhat-ods-operator","relatedImages":{}}` | RHAI Operator configuration |
| rhaiOperator.applicationsNamespace | string | `"redhat-ods-applications"` | Applications namespace |
| rhaiOperator.image | string | `"quay.io/opendatahub/opendatahub-operator:latest"` | Manager container image |
| rhaiOperator.imagePullPolicy | string | `"Always"` | Image pull policy |
| rhaiOperator.namespace | string | `"redhat-ods-operator"` | Operator namespace |
| rhaiOperator.relatedImages | object | `{}` | Related images env vars (RELATED_IMAGE_*) |

