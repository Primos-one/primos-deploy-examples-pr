# primos-deploy Examples

Example configurations for [primos-deploy](https://github.com/Primos-one/primos-deploy-pr) — automated k3s cluster deployment.

## Quick Start

```bash
# Launch primos-deploy-connect (downloads automatically)
./primos-deploy-connect
# → Select host → Create container → server-init runs automatically
# → Demo cluster deployed in ~10 minutes
```

## Configurations

| Config | Topology | Description |
|--------|----------|-------------|
| [1+2 Cluster](https://github.com/Primos-one/primos-deploy-config-1plus2-pr) | 1 server + 2 workers | Minimal production-ready |
| [3+3 Base](https://github.com/Primos-one/primos-deploy-config-3plus3-base-pr) | 3 servers (HA) + 3 workers | HA with embedded etcd |
| [3+3 Infra](https://github.com/Primos-one/primos-deploy-config-3plus3-infra-pr) | 3 servers (HA) + 3 workers + infra | Full stack with monitoring |

Each configuration has a companion `-app-pr` repository with ApplicationSets.

## Demo Keys

Example secrets are encrypted with **demonstration keys** that are embedded in the primos-deploy container.
These keys are public and MUST NOT be used for production. See `DEMO_KEYS.md` in each config repo.

When you're ready to create a real project:
```bash
primos-deploy project create-from-demo
```
This generates real encryption keys and requires new passwords.

## License

MIT
