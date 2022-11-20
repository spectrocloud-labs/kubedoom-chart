# kubedoom-chart

A simple helm chart for demos and examples that embeds noVNC + kubedoom for a "quick" deployment.

## How to use

With helm:

```bash
helm install kubedoom https://github.com/spectrocloud-labs/kubedoom-chart/releases/download/kubedoom-helmchart-0.0.1/kubedoom-helmchart-0.0.1.tgz --set kubedoom_namespace=kube-system
```

or with helm controller:

```yaml
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: kubedoom
  namespace: doom
spec:
  chart: https://github.com/spectrocloud-labs/kubedoom-chart/releases/download/kubedoom-helmchart-0.0.1/kubedoom-helmchart-0.0.1.tgz
  set:
    kubedoom_namespace: "kube-system"
```
## References

- https://github.com/storax/kubedoom  
- https://jhankins.dev/blog/2020/running-novnc-on-kubernetes-to-access-a-machine-on-my-lan/  
