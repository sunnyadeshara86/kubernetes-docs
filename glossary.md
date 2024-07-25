# Kubernetes Glossary

| Term                                  | Definition                                                                                                                                                         |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Admission controller	                | Code that validates or mutates resources to enforce policies. Runs as part of the API admission chain immediately after authentication and authorization.          |
| Annotation                            | Object metadata that can be used to expose alpha or beta capabilities or integrate with third-party systems.                                                       |
| API                                   | Application Programming Interface. In the case of Kubernetes, all resources are defined in the API, which is RESTful and exposed via the API server.               |
| API group                             | A set of related API resources. For example, networking resources are usually located in the networking.k8s.io API group.                                          |
| API resource                          | All Kubernetes objects, such as Pods, Deployments, and Services, are defined in the API as resources.                                                              |
| API Server                            | Exposes the API on a secure port over HTTPS. Runs on the control plane.                                                                                            |
| Cloud controller manager	            |Control plane service that integrates with the underlying cloud platform. For example, when creating a LoadBalancer Service, the cloud controller manager implements the logic to provision one of the underlying cloud’s internet-facing load balancers.                                                                                                                         |
| Cloud native                          | A loaded term that means different things to different people. Cloud native is a way of designing, building, and working with modern applications and infrastructure. I personally consider an application to be cloud native if it can self-heal, scale on-demand, perform rolling updates, and possibly rollbacks.                                               |
| Cluster                               | A set of worker and control plane nodes that work together to run user applications.                                                                               |
| Cluster store                         | Control plane feature that holds the state of the cluster and apps. Typically, it is based on the etcd distributed data store and runs on the control plane. It can be deployed to its own cluster for higher performance and higher availability.                                                                                                                               |
| ConfigMap                             | Kubernetes object used to hold non-sensitive configuration data. A great way to add custom configuration data to a generic container at runtime without editing the image.                                                                                                                                                                                                       |
| Container                             | Lightweight environment for running modern apps. Each container is a virtual operating system with its own process tree, filesystem, shared memory, and more. One container runs one application process.                                                                                                                                                                      |
| Container Network Interface (CNI)     | Pluggable interface enabling different network topologies and architectures. 3rd-parties provide CNI plugins that enable overlay networks, BGP networks, and various implementations of each.                                                                                                                                                                             |
| Container runtime                     | Low-level software running on every cluster Node responsible for pulling container images, starting containers, stopping containers, and other low-level container operations. Typically containerd, Docker, or cri-o. Docker was deprecated in Kubernetes 1.20, and support was removed in 1.24.                                                                               |
| Container Runtime Interface (CRI)     | Low-level Kubernetes feature that allows container runtimes to be pluggable. With the CRI, you can choose the best container runtime for your requirements (Docker, containerd, cri-o, kata, etc.)                                                                                                                                                                               |
| Container Storage Interface (CSI)     | Interface enabling external 3rd-party storage systems to integrate with Kubernetes. Storage vendors write a CSI driver/plugin that runs as a set of Pods on a cluster and exposes the storage system’s enhanced features to the cluster and applications.                                                                                                                  |
| containerd                            | Industry-standard container runtime used in most Kubernetes clusters. Donated to the CNCF by Docker, Inc. Pronounced “container dee”.                              |
| Controller                            | Control plane process running as a reconciliation loop monitoring the cluster and making the necessary changes so the observed state of the cluster matches desired state.                                                                                                                                                                                                       |
| Control plane                         | The brains of every Kubernetes cluster. Comprises the API, API server, scheduler, all controllers, and more. These components run on all control plane nodes of every cluster.                                                                                                                                                                                               |
| control plane node                    | A cluster node hosting control plane services. Usually, it doesn’t run user applications. You should deploy 3 or 5 for high availability.                          |
| cri-o                                 | Container runtime. Commonly used in OpenShift-based Kubernetes clusters.                                                                                           |
| CRUD                                  | The four basic Create, Read, Update, and Delete operations used by many storage systems.                                                                           |
| Custom Resource Definition (CRD)      | API resource used for adding your own resources to the Kubernetes API.                                                                                             |
| Data plane                            | The worker Nodes of a cluster that host user applications.                                                                                                         |
| Deployment                            | Controller that deploys and manages a set of stateless Pods. Performs rollouts and rollbacks, and can self-heal. Uses a ReplicaSet controller to perform scaling and self-healing operations.                                                                                                                                                                                 |
| Desired state                         | What the cluster and apps should be like. For example, the desired state of an application microservice might be five replicas of xyz container listening on port 8080/tcp. Vital to reconciliation.                                                                                                                                                                           |
| Endpoints object                      | Up-to-date list of healthy Pods matching a Service’s label selector. Basically, it’s the list of Pods a Service will send traffic to. Might eventually be replaced by EndpointSlices.                                                                                                                                                                                           |
| etcd                                  | The open-source distributed database used as the cluster store on most Kubernetes clusters.                                                                        |
| Ingress                               | API resource that exposes multiple internal Services over a single external-facing LoadBalancer Service. Operates at layer 7 and implements path-based and host-based HTTP routing.                                                                                                                                                                                          |
| Ingress class                         | API resource that allows you to specify multiple different Ingress controllers on your cluster.                                                                    |
| Init container                        | A specialized container that runs and completes before the main app container starts. Commonly used to check/initialize the environment for the main app container.|
| JSON                                  | JavaScript Object Notation. The preferred format for sending and storing data used by Kubernetes.                                                                  |
| K8s                                   | Shorthand way to write Kubernetes. The “8” replaces the eight characters between the “K” and the “s” of Kubernetes. Pronounced “Kates”. The reason why people say Kubernetes’ girlfriend is called Kate.                                                                                                                                                                       |
| kubectl                               | Kubernetes command line tool. Sends commands to the API server and queries state via the API server.                                                               |
| Kubelet                               | The main Kubernetes agent running on every cluster Node. It watches the API Server for new work assignments and maintains a reporting channel back.                |
| Kube-proxy                            | Runs on every cluster node and implements low-level rules that handle traffic routing from Services to Pods. You send traffic to stable Service names, and kube-proxy makes sure the traffic reaches Pods.                                                                                                                                                                   |
| Label                                 |              |
| Label selector                        |              |
| Manifest file                         |              |
| Microservices                         |              |
| Namespace                             |              |
| Node                                  |              |
| Observed state                        |              |
| Orchestrator                          |              |
| Persistent Volume (PV)                |              |
| Persistent Volume Claim (PVC)         |              |
| Pod                                   |              |
| RBAC                                  |              |
| Reconciliation loop                   |              |
| ReplicaSet                            |              |
| REST                                  |              |
| Secret                                |              |
| Service                               |              |
| Service mesh                          |              |
| Sidecar                               |              |
| StatefulSet                           |              |
| Storage Class (SC)                    |              |
| Volume                                |              |
| WebAssembly (Wasm)                    |              |
| Worker node                           |              |
| YAML                                  |              |
