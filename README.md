# Renovate Shared Config

Shareable Renovate presets for jacaudi repositories.

## Usage

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>jacaudi/renovate-config:base"]
}
```

## Presets

| Preset | Description |
|--------|-------------|
| `local>jacaudi/renovate-config:base` | Base config with common settings and GitHub Actions grouping |
| `local>jacaudi/renovate-config:go` | Go projects - runs `go mod tidy` |
| `local>jacaudi/renovate-config:python` | Python - pins to n-1 version |
| `local>jacaudi/renovate-config:kubernetes` | K8s operators - groups k8s.io packages |
| `local>jacaudi/renovate-config:helm` | Helm charts - groups chart dependencies |
| `local>jacaudi/renovate-config:automerge` | Auto-merge patch updates after 3 days |
| `local>jacaudi/renovate-config:fork` | Enable processing on forked repos |

## Examples

**Go Application:**
```json
{
  "extends": ["local>jacaudi/renovate-config:base", "local>jacaudi/renovate-config:go"]
}
```

**Kubernetes Operator:**
```json
{
  "extends": ["local>jacaudi/renovate-config:base", "local>jacaudi/renovate-config:go", "local>jacaudi/renovate-config:kubernetes"]
}
```

**Python Project:**
```json
{
  "extends": ["local>jacaudi/renovate-config:base", "local>jacaudi/renovate-config:python"]
}
```

## Base Settings

- Timezone: America/Los_Angeles
- Semantic commits: `chore(deps): ...`
- Dashboard enabled
- Assignees: jacaudi
- Labels: renovate
- GitHub Actions grouped
