# Talos cluster config

## Generating machine config

```bash
talosctl gen config \
  --with-secrets secrets.yaml \
  --config-patch-control-plane @controlplane-patch.yml \
  --output-types controlplane \
  talos https://192.168.1.6:6443
```

## Applying configuration

```bash
talosctl apply-config -f ./controlplane.yaml
```

### For use with Tailscale

```bash
talosctl apply-config -f ./controlplane.yaml -p @tailscale.patch.yaml
```

## References

- https://www.talos.dev/v1.9/introduction/prodnotes/
