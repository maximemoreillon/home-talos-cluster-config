# Talos cluster config

Generating machine config file:

```bash
talosctl gen config \
  --with-secrets ../secrets.yaml \
  --config-patch-control-plane @controlplane-patch.yml \
  talos https://192.168.1.27:6443
```

## References

- https://www.talos.dev/v1.9/introduction/prodnotes/
