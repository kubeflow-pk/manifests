# manifests



| 模块          | 子模块                             | 功能     | 镜像（kubeflow1.0.2）                                        | 编译(arm) | 运行（arm） | 编译（x86） | 运行（x86） | 镜像（kubeflow1.1.0） | 备注 |
| ------------- | ---------------------------------- | -------- | ------------------------------------------------------------ | --------- | ----------- | ----------- | ----------- | --------------------- | ---- |
| Dashboard     | centraldashboard                   | **核心** | gcr.io/kubeflow-images-public/centraldashboard:v1.0.0-g3ec0de71 | ✅         | ✅           | ✅           | ✅           |                       |      |
| Notebook      | jupyter-web-app                    | **核心** | gcr.io/kubeflow-images-public/jupyter-web-app:v0.5.0         | ✅         | ✅           | ✅           | ✅           |                       |      |
| Notebook      | Notebook-controller                | **核心** | gcr.io/kubeflow-images-public/notebook-controller:v20190614-v0-160-g386f2749-e3b0c4 | ✅         | ✅           | ✅           | ✅           |                       |      |
| Profile       | profiles                           | **核心** | gcr.io/kubeflow-images-public/profile-controller:v20190619-v0-219-gbd3daa8c-dirty-1ced0e | ✅         | ❌           | ✅           | ✅           |                       |      |
| Profile       | profiles                           | **核心** | gcr.io/kubeflow-images-public/kfam:v20190612-v0-170-ga06cdb79-dirty-a33ee4 | ✅         | ✅           | ✅           | ✅           |                       |      |
| Application   | application                        | 未知     | gcr.io/kubeflow-images-public/kubernetes-sigs/application:1.0-beta | ✅         | ❌           | ✅           | ✅           |                       |      |
| Application   | application-crds                   | 未知     | 无镜像                                                       |           |             |             |             |                       |      |
| Pipeline      | persistent-agent                   | **核心** | gcr.io/ml-pipeline/persistenceagent:0.2.5                    | ✅         | 待测试      | ✅           | ✅           |                       |      |
| Pipeline      | pipelines-runner                   | **核心** | 无镜像                                                       |           |             |             |             |                       |      |
| Pipeline      | pipelines-ui                       | **核心** | gcr.io/ml-pipeline/frontend                                  | ✅         | 待测试      | ✅           | ✅           |                       |      |
| Pipeline      | pipelines-viewer                   | **核心** | gcr.io/ml-pipeline/viewer-crd-controller:0.1.31              | ✅         | 待测试      | ✅           | ✅           |                       |      |
| Pipeline      | pipeline-visualization-service     | 依赖     | gcr.io/ml-pipeline/visualization-server:0.2.5                | ❌         | ❌           | ✅           | ✅           |                       |      |
| Pipeline      | api-service                        | **核心** | gcr.io/ml-pipeline/api-server:0.2.5                          | ❌         | ❌           | ✅           | ✅           |                       |      |
| Pipeline      | scheduledworkflow                  |          | gcr.io/ml-pipeline/scheduledworkflow:0.2.5                   | ✅         | ❌           | ✅           | ✅           |                       |      |
| Istio/ingress | add-anonymous-user-filter          | 未知     | 无镜像                                                       |           |             |             |             |                       |      |
| Istio/ingress | bootstrap                          | 未使用   | gcr.io/kubeflow-images-public/ingress-setup:latest           |           |             |             |             |                       |      |
| Istio/ingress | istio                              | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Istio/ingress | istio-crds                         | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Istio/ingress | istio-install                      | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Istio/ingress | cluster-local-gateway              | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Cert          | cert-manager                       | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Cert          | cert-manager-crds                  | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Cert          | cert-manager-kube-system-resources | 暂不使用 |                                                              |           |             |             |             |                       |      |
| Katib         | katib-controller                   | 依赖     | gcr.io/kubeflow-images-public/katib/v1alpha3/katib-controller:v0.8.0 |           |             |             |             |                       |      |
| Katib         | katib-controller                   | 依赖     | gcr.io/kubeflow-images-public/katib/v1alpha3/katib-db-manager:v0.8.0 |           |             |             |             |                       |      |
| Katib         | katib-controller                   | 依赖     | gcr.io/kubeflow-images-public/katib/v1alpha3/katib-ui:v0.8.0 |           |             |             |             |                       |      |
| Katib         | katib-controller                   |          | mysql:8                                                      |           |             |             |             |                       |      |
| Katib         | katib-crds                         | 依赖     | 无镜像                                                       |           |             |             |             |                       |      |
| Kfserving     | kfserving-crds                     | 依赖     | 无镜像                                                       |           |             |             |             |                       |      |
| Kfserving     | kfserving-gateway                  | 依赖     | docker.io/istio/proxyv2:1.1.6                                |           |             |             |             |                       |      |
| Kfserving     | kfserving-install                  | 依赖     | gcr.io/kubebuilder/kube-rbac-proxy:v0.4.0                    |           |             |             |             |                       |      |
| Kfserving     | kfserving-install                  | 依赖     | gcr.io/kfserving/kfserving-controller:0.2.2                  |           |             |             |             |                       |      |
| Knative       | knative-crds                       | 依赖     | 无镜像                                                       |           |             |             |             |                       |      |
| Knative       | knative-install                    | 依赖     | gcr.io/knative-releases/knative.dev/serving/cmd/controller@sha256:5ca13e5b3ce5e2819c4567b75c0984650a57272ece44bc1dabf930f9fe1e19a1 |           |             |             |             |                       |      |
| Knative       | knative-install                    | 依赖     | gcr.io/knative-releases/knative.dev/serving/cmd/webhook@sha256:1ef3328282f31704b5802c1136bd117e8598fd9f437df8209ca87366c5ce9fcb |           |             |             |             |                       |      |
| Knative       | knative-install                    | 依赖     | gcr.io/knative-releases/knative.dev/serving/cmd/networking/istio@sha256:727a623ccb17676fae8058cb1691207a9658a8d71bc7603d701e23b1a6037e6c |           |             |             |             |                       |      |
| Knative       | knative-install                    | 依赖     | gcr.io/knative-releases/knative.dev/serving/cmd/autoscaler@sha256:ef1f01b5fb3886d4c488a219687aac72d28e72f808691132f658259e4e02bb27 |           |             |             |             |                       |      |
| Knative       | knative-install                    | 依赖     | gcr.io/knative-releases/knative.dev/serving/cmd/autoscaler-hpa@sha256:5e0fadf574e66fb1c893806b5c5e5f19139cc476ebf1dff9860789fe4ac5f545 |           |             |             |             |                       |      |
| Knative       | knative-install                    | 依赖     | gcr.io/knative-releases/knative.dev/serving/cmd/activator@sha256:8e606671215cc029683e8cd633ec5de9eabeaa6e9a4392ff289883304be1f418 |           |             |             |             |                       |      |
| Kubeflow      | kubeflow-roles                     | 依赖     | 无镜像                                                       |           |             |             |             | M                     |      |
| Metadata      | metacontroller                     | 依赖     | metacontroller/metacontroller:v0.3.0                         |           |             |             |             |                       |      |
| Metadata      | metadata                           | 依赖     | gcr.io/kubeflow-images-public/metadata:v0.1.11               |           |             |             |             |                       |      |
| Metadata      | metadata                           | 依赖     | gcr.io/tfx-oss-public/ml_metadata_store_server:v0.21.1       |           |             |             |             |                       |      |
| Metadata      | metadata                           | 依赖     | gcr.io/ml-pipeline/envoy:metadata-grpc                       |           |             |             |             |                       |      |
| Metadata      | metadata                           | 依赖     | gcr.io/kubeflow-images-public/metadata-frontend:v0.1.8       |           |             |             |             |                       |      |
| Metadata      | metadata                           | 依赖     | mysql:8.0.3                                                  |           |             |             |             |                       |      |
| Webhook       | webhook                            | 依赖     | gcr.io/kubeflow-images-public/admission-webhook:v20190520-v0-139-gcee39dbc-dirty-0d8f4c |           |             |             |             |                       |      |
| Minio         | Minio                              | 依赖     | minio/minio:RELEASE.2018-02-09T22-40-05Z                     |           |             |             |             |                       |      |
| mysql         | mysql                              | 依赖     | mysql:5.6                                                    |           |             |             |             |                       |      |
|               |                                    |          |                                                              |           |             |             |             |                       |      |



