# Dual-site kustomize-ed app

This Kubernetes app leverages kustomize to expose web services with different configurations;
for example, if two identical web services must run on different sites,
they have to pull the images from local registries and also be exposed to different domains.

There's a [common base layer](./bases) and site-specific customisations ([site-1](./site-1) and [site.2](./site-2)).
The site-specific configurations have to be applied on each site, as in

```shell
kubectl apply -k site-1
```

Plain manifests can be generated with the `kustomize build` command, which is also integrated into `kubectl`:

```shell
kubectl kustomize site-1
```
