## References 
- https://github.com/deliveryhero/helm-charts/tree/master/stable/locust

## Prerequisite to create deploy locust
- If HPA needs to be enabled for locust worker then it is required to have matrix server installed in cluster.

### Enable HPA on locust worker nodes in ivari-sandbox-values.yaml
```yaml
worker:
  hpa:
    enabled: true
  resources:
    limits:
      cpu: 500m
      memory: 256Mi
    requests:
      cpu: 500m
      memory: 256Mi
```
