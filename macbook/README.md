# linkerd install
run first 
``` bash 
step certificate create root.linkerd.cluster.local ca.crt ca.key \
  --profile root-ca --no-password --insecure &&
  kubectl create secret tls \
    linkerd-trust-anchor \
    --cert=ca.crt \
    --key=ca.key \
    --namespace=linkerd
```