```
#!/bin/bash
kubectl create secret docker-registry quay-key \
  --docker-server=quay.io \
  --docker-username=whiskhq \
  --docker-password=password \
  --docker-email=tech@whisk.co.uk
```

## Deploy traefik

```
helm install --name traefik --namespace kube-system --values traefik/values.yaml stable/traefik
```