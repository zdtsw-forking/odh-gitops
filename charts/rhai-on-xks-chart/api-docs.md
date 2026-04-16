# rhai-on-xks-chart

![Version: 3.4.0-ea.2](https://img.shields.io/badge/Version-3.4.0--ea.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.4.0-ea.2](https://img.shields.io/badge/AppVersion-3.4.0--ea.2-informational?style=flat-square)

Red Hat OpenShift AI Operator Helm chart (non-OLM installation)

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| azure.cloudManager.image | string | `"registry.redhat.io/rhoai/odh-rhel9-operator@sha256:67d8ad67bef9ce7d06f66a0a3fc054052962f1e59c96629ecadc6790f319f1d1"` |  |
| azure.cloudManager.imagePullPolicy | string | `"Always"` |  |
| azure.cloudManager.namespace | string | `"rhai-cloudmanager-system"` |  |
| azure.enabled | bool | `false` |  |
| azure.kubernetesEngine.enabled | bool | `true` |  |
| azure.kubernetesEngine.spec.dependencies.certManager.configuration | object | `{}` |  |
| azure.kubernetesEngine.spec.dependencies.certManager.managementPolicy | string | `"Managed"` |  |
| azure.kubernetesEngine.spec.dependencies.gatewayAPI.configuration | object | `{}` |  |
| azure.kubernetesEngine.spec.dependencies.gatewayAPI.managementPolicy | string | `"Managed"` |  |
| azure.kubernetesEngine.spec.dependencies.lws.configuration | object | `{}` |  |
| azure.kubernetesEngine.spec.dependencies.lws.managementPolicy | string | `"Managed"` |  |
| azure.kubernetesEngine.spec.dependencies.sailOperator.configuration | object | `{}` |  |
| azure.kubernetesEngine.spec.dependencies.sailOperator.managementPolicy | string | `"Managed"` |  |
| components.kserve.enabled | bool | `true` |  |
| components.kserve.spec | object | `{}` |  |
| coreweave.cloudManager.image | string | `"registry.redhat.io/rhoai/odh-rhel9-operator@sha256:67d8ad67bef9ce7d06f66a0a3fc054052962f1e59c96629ecadc6790f319f1d1"` |  |
| coreweave.cloudManager.imagePullPolicy | string | `"Always"` |  |
| coreweave.cloudManager.namespace | string | `"rhai-cloudmanager-system"` |  |
| coreweave.enabled | bool | `false` |  |
| coreweave.kubernetesEngine.enabled | bool | `true` |  |
| coreweave.kubernetesEngine.spec.dependencies.certManager.configuration | object | `{}` |  |
| coreweave.kubernetesEngine.spec.dependencies.certManager.managementPolicy | string | `"Managed"` |  |
| coreweave.kubernetesEngine.spec.dependencies.gatewayAPI.configuration | object | `{}` |  |
| coreweave.kubernetesEngine.spec.dependencies.gatewayAPI.managementPolicy | string | `"Managed"` |  |
| coreweave.kubernetesEngine.spec.dependencies.lws.configuration | object | `{}` |  |
| coreweave.kubernetesEngine.spec.dependencies.lws.managementPolicy | string | `"Managed"` |  |
| coreweave.kubernetesEngine.spec.dependencies.sailOperator.configuration | object | `{}` |  |
| coreweave.kubernetesEngine.spec.dependencies.sailOperator.managementPolicy | string | `"Managed"` |  |
| enabled | bool | `true` |  |
| imagePullSecret.dependencyNamespaces[0] | string | `"cert-manager-operator"` |  |
| imagePullSecret.dependencyNamespaces[1] | string | `"cert-manager"` |  |
| imagePullSecret.dependencyNamespaces[2] | string | `"openshift-lws-operator"` |  |
| imagePullSecret.dependencyNamespaces[3] | string | `"istio-system"` |  |
| imagePullSecret.dockerConfigJson | string | `""` |  |
| imagePullSecret.name | string | `"rhaii-pull-secret"` |  |
| installCRDs | bool | `true` |  |
| labels | object | `{}` |  |
| rhaiOperator.applicationsNamespace | string | `"redhat-ods-applications"` |  |
| rhaiOperator.image | string | `"registry.redhat.io/rhoai/odh-rhel9-operator@sha256:67d8ad67bef9ce7d06f66a0a3fc054052962f1e59c96629ecadc6790f319f1d1"` |  |
| rhaiOperator.imagePullPolicy | string | `"Always"` |  |
| rhaiOperator.namespace | string | `"redhat-ods-operator"` |  |
| rhaiOperator.relatedImages[0].name | string | `"RELATED_IMAGE_ODH_MAAS_API_IMAGE"` |  |
| rhaiOperator.relatedImages[0].value | string | `"registry.redhat.io/rhoai/odh-maas-api-rhel9@sha256:4688044ef66cc27ca34e595d19da5d94d330ed27c6d7953887e3834694dcce20"` |  |
| rhaiOperator.relatedImages[10].name | string | `"RELATED_IMAGE_OSE_KUBE_RBAC_PROXY_IMAGE"` |  |
| rhaiOperator.relatedImages[10].value | string | `"registry.redhat.io/rhoai/odh-kube-auth-proxy-rhel9@sha256:f118fd73be911e899d5aff76b4ca599d10c73e4cc4bf803204734e7f6aeb44c2"` |  |
| rhaiOperator.relatedImages[1].name | string | `"RELATED_IMAGE_ODH_KSERVE_CONTROLLER_IMAGE"` |  |
| rhaiOperator.relatedImages[1].value | string | `"registry.redhat.io/rhoai/odh-kserve-controller-rhel9@sha256:4f630af88329826cdfb7faddd3d8a75a019fe971f9c027f4720a94a52f0638f9"` |  |
| rhaiOperator.relatedImages[2].name | string | `"RELATED_IMAGE_ODH_KSERVE_LLMISVC_CONTROLLER_IMAGE"` |  |
| rhaiOperator.relatedImages[2].value | string | `"registry.redhat.io/rhoai/odh-kserve-llmisvc-controller-rhel9@sha256:19ab9bef5b38b0d97a84361b4bc80b9ba30b42d85cd96cd78e60d4922ead3ef8"` |  |
| rhaiOperator.relatedImages[3].name | string | `"RELATED_IMAGE_ODH_KSERVE_ROUTER_IMAGE"` |  |
| rhaiOperator.relatedImages[3].value | string | `"registry.redhat.io/rhoai/odh-kserve-router-rhel9@sha256:706392ecb4f3c389ca1ce0ec87640ed6745bc176246c1edf3963e1c0357e284a"` |  |
| rhaiOperator.relatedImages[4].name | string | `"RELATED_IMAGE_ODH_KSERVE_STORAGE_INITIALIZER_IMAGE"` |  |
| rhaiOperator.relatedImages[4].value | string | `"registry.redhat.io/rhoai/odh-kserve-storage-initializer-rhel9@sha256:eb925c1a0c46fbbda626688c576dc2d4f958d0b7a128132cb8e8c30ec5442df8"` |  |
| rhaiOperator.relatedImages[5].name | string | `"RELATED_IMAGE_RHAIIS_VLLM_CUDA_IMAGE"` |  |
| rhaiOperator.relatedImages[5].value | string | `"registry.redhat.io/rhaii-early-access/vllm-cuda-rhel9@sha256:abf0fd7398a18c47a754218b0cbd76ea300b0c6da5fb8d801db8c165df5022ca"` |  |
| rhaiOperator.relatedImages[6].name | string | `"RELATED_IMAGE_RHAIIS_VLLM_ROCM_IMAGE"` |  |
| rhaiOperator.relatedImages[6].value | string | `"registry.redhat.io/rhaii-early-access/vllm-rocm-rhel9@sha256:6c566f161c3102942855cdbef6e10580b8dc61f61bc85b5206d7b5e67bfadef0"` |  |
| rhaiOperator.relatedImages[7].name | string | `"RELATED_IMAGE_ODH_LLM_D_INFERENCE_SCHEDULER_IMAGE"` |  |
| rhaiOperator.relatedImages[7].value | string | `"registry.redhat.io/rhoai/odh-llm-d-inference-scheduler-rhel9@sha256:e5f154ac40919f46f1d46902cb701ee7fa9c611f54dcc923f2098c33c47d2238"` |  |
| rhaiOperator.relatedImages[8].name | string | `"RELATED_IMAGE_ODH_LLM_D_KV_CACHE_IMAGE"` |  |
| rhaiOperator.relatedImages[8].value | string | `"registry.redhat.io/rhoai/odh-llm-d-kv-cache-rhel9@sha256:cdf0f45fd7bbbd4adbb4a626962211d48de3c9f5c7544f500167060c5e73936c"` |  |
| rhaiOperator.relatedImages[9].name | string | `"RELATED_IMAGE_ODH_LLM_D_ROUTING_SIDECAR_IMAGE"` |  |
| rhaiOperator.relatedImages[9].value | string | `"registry.redhat.io/rhoai/odh-llm-d-routing-sidecar-rhel9@sha256:dcbcbcc5051dcabda5b207175b2cf64f3ef133f4c7de8204103e975dfde37351"` |  |

