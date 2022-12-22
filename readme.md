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
