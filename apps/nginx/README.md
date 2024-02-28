# Sample nginx app

This is a sample Kubernetes app exposing a web service, defined via plain manifest files.

The manifests must be comprehensive and specify every single detail of the Kubernetes resources:
i.e. containers' images, security context, ...

__N.B.__ This example uses VMware AVI Load Balancer, and the default TLS secret capability
via the `ako.vmware.com/enable-tls: "true"` annotation.
