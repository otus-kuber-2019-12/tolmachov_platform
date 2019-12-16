# tolmachov_platform

## kubernetes-intro

 1. The reason for restarting the containers is described in the PR description;
 2. an image was created based on the `nginx:latest` image, starting from a user with UID #1001;
 3. manifest `web-pod.yaml` was created;
 4. manifest `frontend-pod.yaml` was generated;
 5. manifest `frontend-pod.yaml` was fixed and saved as `frontend-pod-healthy.yaml`.

### Run

Run web:

```bash
kubectl apply -f web-pod.yaml
kubectl port-forward web 8000:8000
```

Run frontend:

```bash
kubectl apply -f frontend-pod-healthy.yaml
sudo kubectl port-forward web 8080:8080
```
