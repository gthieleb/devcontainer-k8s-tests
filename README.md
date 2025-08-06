devcontainer setup using Guacomole or KasmVNC to evaluate each possibilities.

## traefik
using this setup:

https://github.com/jcchavezs/traefik-kind/blob/main/kind-config.yaml

## kasmvnc

KasmVNC offers ready to use images for VSCode that can be used via browser. This can be used standalone. Alternative external RDP, VNC services can be connected.

KasmVNC install is possible via helm:

https://github.com/kasmtech/kasm-helm

KasmVNC supports OIDC auth:

https://github.com/kasmtech/KasmVNC/issues/300

## Guacomole:

Guacomole can be used together with external RDP, VNC services. This can be VM or XRDP or X11VNC containers served via docker/podman/kubernetes.

cnpg is dependency:

```
helm repo add cnpg https://cloudnative-pg.github.io/charts
helm upgrade --install cnpg \
  --namespace cnpg-system \
  --create-namespace \
  cnpg/cloudnative-pg
```

guacomole from truecharts:

```
helm install mychart oci://tccr.io/truecharts/guacamole
```
