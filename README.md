# simple-k8s-deploy action

This action deploys to a locally available Kubernetes cluster (you have to have a correct `ServiceAccount` attached to your runner pods). A kubectl and yq would be downloaded before conducting a deployment.

## Inputs

## `kubectl_version`

kubectl binary version. Default `"1.28.2"`.

## `manifest_filepath`

Path to a Kubernetes deployment manifest. Default `"kubernetes/deployment.yaml"`.

## `container_name`

**Required** Container name that would have it's image overwritten inside the deployment manifest.

## `image_name`

**Required** Image name that would be overwritten inside the deployment manifest.

## Outputs

## `kubectl-apply`

Result of kubectl apply.

## Example usage

```yaml
uses: thesharp/simple-k8s-deploy@v1
with:
    container_name: "application"
    image_name: "ghcr.io/user/application:1.55"
```
