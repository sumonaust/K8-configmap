# ConfigMap in Kubernetes

Before starting with this tutorial, you should have a basic understanding of Kubernetes and how to create a pod, service, and deployment. You should also have the kubectl command-line tool installed and configured to interact with your Kubernetes cluster.

## Commands used for Configmap
To create a ConfigMap from a literal value, use the following command:
```
kubectl create configmap configmap-1 --from-literal=name=first-configmap
```

To create a ConfigMap from multiple literal values, use the following command:
```
kubectl create configmap configmap-2 --from-literal=name=second-configmap --from-literal=color=blue
```

To create a ConfigMap from a file, use the following command:
```
kubectl create configmap configmap-3 --from-file=data-file
```

To apply the YAML files provided in this repository, use the following command:
```
kubectl apply -f <file-name.yaml>
```

To see the pods running in your Kubernetes cluster, use the following command:
```
kubectl get pods
```

To see the ConfigMaps created in your Kubernetes cluster, use the following command:
```
kubectl get cm
```

To see the environment variables set in a running pod, use the following command:
```
kubectl exec -it <pod-name> -- printenv
```

To go inside a running pod, use the following command:
```
kubectl exec -it <pod-name> -- bash
```

## Summary
In this tutorial, you learned how to use ConfigMaps to manage configuration data in your Kubernetes cluster. ConfigMaps can be used to store configuration data as key-value pairs or as files. You can then use environment variables or volume mounts to make this data available to your applications running in Kubernetes.
