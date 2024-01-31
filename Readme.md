# Way - 2

Need the cluster running and argocd installed. Install by readme.md in gitrepo way-1

# Apply this manifest CRD Application

```
kubectl apply -f application.yaml
```

# Create app in argocd cli

```
argocd app create way-2 --repo https://github.com/desafioaltbank/way-2.git --path . --dest-server https://kuberne
tes.default.svc --sync-policy automated --sync-retry-limit 5 --self-heal --auto-prune --dest-namespace argocd
```
