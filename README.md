# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) configs for all projectpotos
repositories.

## Usage

Add a `renovate.json` to the repository:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>projectpotos/renovate-config"]
}
```

Specs repositories can use
the `ansible` preset:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>projectpotos/renovate-config:ansible"]
}
```

## Presets

### `default`

* Based on [`config:best-practices`](https://docs.renovatebot.com/presets-config/#configbest-practices)
* 7-day cooldown (`minimumReleaseAge`) on new releases, except for
  projectpotos' own actions, workflows and images.
* No automerge: every update is a pull request that goes through review.
* Dependency dashboard issue enabled.

### `ansible`

The `ansible` config extend `default` with additional support to manage ansible dependencies in  `base-requirements.yml`.
