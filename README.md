# Renovate Shared Config

Shareable Renovate presets for jacaudi repositories.

## Usage

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>jacaudi/renovate-config:base"]
}
```

## Presets

| Preset | Description |
|--------|-------------|
| `base` | Base config with common settings and GitHub Actions grouping |
| `go` | Go projects - runs `go mod tidy` |
| `python` | Python - pins to n-1 version |
| `kubernetes` | K8s operators - groups k8s.io packages |
| `helm` | Helm charts - groups chart dependencies |
| `automerge` | Auto-merge patch updates after 3 days |
| `fork` | Enable processing on forked repos |

## Example

```json
{
  "extends": [
    "github>jacaudi/renovate-config:base",
    "github>jacaudi/renovate-config:go",
    "github>jacaudi/renovate-config:kubernetes"
  ]
}
```
