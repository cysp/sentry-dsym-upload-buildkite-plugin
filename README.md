# sentry-dsym-upload-buildkite-plugin

A [Buildkite](https://buildkite.com/) plugin to upload iOS app debugging symbols to [Sentry](https://sentry.io/).

## Example

```yml
steps:
  - name: ":package:"
    command: .ci-scripts/build-and-archive.sh
    env:
      SENTRY_ORG: organization
      SENTRY_PROJECT: project
    plugins:
      sentry-dsym-upload:
        path: .ci-artifacts/Xyzzy.app.dSYM
```

## Configuring

### `SENTRY_AUTH_TOKEN`

## Options

### `auth-token`

Specifies the Sentry authentication token

### `auth-token-from`

Specifies the environment variable containing the Sentry authentication token

Default: `SENTRY_AUTH_TOKEN`

### `org`

Specifies the Sentry organization slug

### `org-from`

Specifies the environment variable containing the Sentry organization slug

Default: `SENTRY_ORG`

### `project`

Specifies the Sentry project slug

### `project-from`

Specifies the environment variable containing the Sentry project slug

Default: `SENTRY_PROJECT`

### `path`

Specifies the path to the .dSYM to upload

## License

MPL 2.0 (see [LICENSE](LICENSE))
