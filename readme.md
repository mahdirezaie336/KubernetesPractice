# Kubernetes Commands

1. Get nodes to see if node is running

    ```bash
    kubectl get node
    ```

2. Run a pod

    ```bash
    kubectl run <Pod Name> --image=<Image Name>
    ```

3. Get pods to see if pod is running

    ```bash
    kubectl get pod
    ```

4. See logs of pod to see levels of errors

    ```bash
    kubectl logs <Pod Name>
    ```

5. Describe pod to see more details

    ```bash
    kubectl describe pod <Pod Name>
    ```

6. Delete pod

    ```bash
    kubectl delete pod <Pod Name>
    ```

7. Create a deployment to manage a pod if it fails

    ```bash
    kubectl create deployment <Deployment Name> --image=<Image Name>
    ```

8. Get deployments to see if deployment is running

   ```bash
   kubectl get deployments.apps
   ```

9. Delete a pod

    ```bash
    kubectl detele pod <Pod Name>
    ```

10. Delete a deployment

    ```bash
    kubectl delete deployment <Deployment Name>
    ```

11. Create a deployment and output yaml

    ```bash
    kubectl create deployment <Deployment Name> --image=<Image Name> --dry-run=client -o yaml
    ```

12. Apply a deployment from a yaml file

    ```bash
    kubectl apply -f <Deployment Name>.yaml
    ```

13. Get more info from a pod to a file

    ```bash
    kubectl describe pod <Pod Name> -o wide
    ```

14. Get api resources

    ```bash
    kubectl api-resources
    ```

15. Create a secret

    ```bash
    kubectl create secret generic <Secret Name> --from-literal=<Key>=<Value>
    ```

16. Apply a secret from a yaml file

    ```bash
    kubectl apply -f <Secret Name>.yaml
    ```

17. Use secret in a pod container

    ```bash
    env:
      - name: <Key>
        valueFrom:
          secretKeyRef:
            name: <Secret Name>
            key: <Key>
    ```

18. Explain a resource

    ```bash
    kubectl explain <Resource Name>
    ```

    Example:

    ```bash
    kubectl explain pod.spec
    kubeclt explain pod.spec.containers
    ```

19. Get endpoints

    ```bash
    kubectl get endpoints
    kubeclt get ep
    ```

20. Get services

    ```bash
    kubectl get services
    kubeclt get svc
    ```

21. Create a service and output yaml

    ```bash
    kubectl create service clusterip <Service Name> --tcp=<Port>:<Port> --dry-run=client -o yaml
    ```

22. Create a volume and output yaml

    ```bash
    kubectl create volume <Volume Name> --dry-run=client -o yaml
    ```

23. Claim a volume

    ```bash
    kubectl create volume claim <Volume Name> --dry-run=client -o yaml
    ```

## YAML Files

1. What is selector?

    ```yaml
    selector:
      matchLabels:
        app: <Label Name>
    ```

    It is used to match the label of the pod to the label of the deployment.

## How to use?

1. Create config map using this command

    ```bash
    kubectl create configmap <Config Map Name> --from-literal=<Key>=<Value>
    ```
