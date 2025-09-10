## Prometheus
- https://github.com/prometheus-operator/kube-prometheus/tree/release-0.16 (Installed)

# Ingress-Nginx
- https://github.com/nginx/kubernetes-ingress/tree/v5.1.1 (Installed)
- https://github.com/kubernetes/ingress-nginx/tree/release-1.13 (Not installed)

# Descheduler
- https://github.com/kubernetes-sigs/descheduler/tree/release-1.33

## Flux system repository
```sh
flux install --components-extra image-reflector-controller,image-automation-controller --export > ./clusters/home-k3s/flux-system/gotk-components.yaml

flux bootstrap git --url=ssh://git@github.com/SShymchuk/home-k3s-cluster.git --branch=main --path=clusters/home-k3s --components-extra=image-reflector-controller,image-automation-controller --private-key-file=<path_to_file>  --password=<> --kubeconfig ~/.kube/config
```