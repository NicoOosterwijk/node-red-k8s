# Node-RED kustomization K8s

```
apiVersion: fleet.cattle.io/v1alpha1
kind: GitRepo
metadata:
  name: home-assistant
  namespace: fleet-default
  labels:
    node-red: enabled
spec:
  branch: main
  clientSecretName: auth-hp48c
  repo: https://github.com/NicoOosterwijk/node-red-k8s.git
  targets:
    - clusterGroup: node-red
```