# Instructions

## Patching CoreDNS

Run the following command after fixing `~/.kube/config` and `/etc/kubernetes/manifests/kube-apiserver.yaml`:

```kubectl patch deployment coredns -n kube-system -p '{"spec":{"template":{"spec":{"containers":[{"name":"coredns", "image":"registry.k8s.io/coredns/coredns:v1.8.6"}]}}}}'```

## Allow scheduling on `node01`

`kubectl uncordon node01`

## Copy files from /media to /web

`scp /media/* node01:/web/`
