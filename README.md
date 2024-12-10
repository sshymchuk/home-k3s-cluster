## Flux system repository
```sh
flux install --components-extra image-reflector-controller,image-automation-controller --export > ./clusters/home-k3s/flux-system/gotk-components.yaml

flux bootstrap git --url=ssh://git@github.com/SShymchuk/home-k3s-cluster.git --branch=main --path=clusters/home-k3s --components-extra=image-reflector-controller,image-automation-controller --private-key-file=<path_to_file>  --password=<> --kubeconfig ~/.kube/config
```