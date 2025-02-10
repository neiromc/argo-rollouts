### promote rollout
https://github.com/argoproj/argo-rollouts/blob/master/pkg/kubectl-argo-rollouts/cmd/promote/promote.go#L39
```bash
golang: promoteFullPatch        = `{"status":{"promoteFull":true}}`

kubectl -n <namespace> patch rollouts.argoproj.io <rollout-name> --type=merge --subresource status -p '{"status":{"promoteFull":true}}'
```

### abort rollout
https://github.com/argoproj/argo-rollouts/blob/master/pkg/kubectl-argo-rollouts/cmd/abort/abort.go#L30
```bash
golang: abortPatch              = `{"status":{"abort":true}}`

kubectl -n <namespace> patch rollouts.argoproj.io <rollout-name> --type=merge --subresource status -p '{"status":{"abort":true}}'
```