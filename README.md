## Sandboxes for argo rollouts

### promote-abort
Contains manifests for promote and abort argo rollouts using gitops. Manifests is auto removed if completed successful after spec.ttlSecondsAfterFinished seconds (defined in job manifest). The `rbac.yaml` is common for both manifests and must applied once.

### canary
- Simple canary strategy with header.
```bash
kubectl apply -f /canary/v1/ns.yaml   #create ns
kubectl apply -f /canary/v1/all.yaml  #apply app manifests
```
<img src=canary/v1/canary_v1.svg>



