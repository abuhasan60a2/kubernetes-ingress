# Kubernetes Ingress

## Overview

This repository contains the code and configuration files for setting up Kubernetes Ingress. The Ingress resource allows you to define how external traffic is routed to your services within a Kubernetes cluster.

## Prerequisites

- Kubernetes cluster (v1.19+)
- kubectl configured to interact with your cluster
- Ingress controller installed (e.g., NGINX Ingress Controller)

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/kubernetes-ingress.git
cd kubernetes-ingress
```

### 2. Deploy the Application

Apply the Kubernetes manifests to deploy the application and the Ingress resource.

```sh
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
```

### 3. Verify the Deployment

Check the status of the pods to ensure they are running.

```sh
kubectl get pods
```

### 4. Access the Application

Once the Ingress resource is created, you can access the application using the external IP or DNS name of the Ingress controller.

```sh
http://<ingress-controller-ip>
```

## How It Works

### Deployment

The `deployment.yaml` file defines the deployment of your application, specifying the number of replicas, container image, and other configurations.

### Service

The `service.yaml` file defines a Kubernetes Service that exposes your application to other pods within the cluster.

### Ingress

The `ingress.yaml` file defines the Ingress resource, which specifies the rules for routing external HTTP(S) traffic to your services. The Ingress controller processes these rules and configures the necessary load balancers or proxies.

## Files

- `deployment.yaml`: Defines the deployment of the application.
- `service.yaml`: Defines the service to expose the application.
- `ingress.yaml`: Defines the ingress rules for routing traffic.

## Conclusion

By following the steps above, you can deploy and expose your application using Kubernetes Ingress. This setup allows you to manage external access to your services in a flexible and scalable manner.

For more information, refer to the [Kubernetes Ingress documentation](https://kubernetes.io/docs/concepts/services-networking/ingress/).
