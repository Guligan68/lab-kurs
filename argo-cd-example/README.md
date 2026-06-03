# Argo CD Deployment Example

This is a minimum example of how to structure a repository for Argo CD.

## Structure

- `manifests/`: Contains the raw Kubernetes manifests for the application.
    - `app.yaml`: A simple Deployment and Service (Guestbook UI).
- `application.yaml`: An Argo CD `Application` resource that defines where the app should be deployed and which manifests to use.

## How to use

1.  **Install Argo CD** in your Kubernetes cluster if you haven't already.
2.  **Apply the Application manifest**:
    ```bash
    kubectl apply -f argo-cd-example/application.yaml
    ```

*Note: In a real scenario, you would update the `repoURL` in `application.yaml` to point to your own repository and the `path` to point to `argo-cd-example/manifests`.*
