# Kustomize-ed nginx app

This Kubernetes app exposes a web service, making use of Kustomize to apply customisations.

The manifests can be simpler, thus more readable, than the [nginx example](../nginx/),
because they can be further customised declaratively via the `kustomization.yaml` file:

- containers' images and tags can be changed, to point to different registries
- every resoiurce can be patched, i.e. pods' containers can be patched to define the `securityContext` section, to make the pod pass the [Pod Security Admission](https://kubernetes.io/docs/concepts/security/pod-security-admission/).

The manifests can be rendered and applied via

```shell
kubectl apply -k .
```

Plain manifests can be generated with the `kustomize build` command, which is also integrated into `kubectl`:

```shell
kubectl kustomize
```
