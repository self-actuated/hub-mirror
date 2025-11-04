# hub-mirror

GitHub Action to configure a Docker Hub mirror for actuated servers.

* Writes /etc/docker/daemon.json to use the mirror and trust its CA
* Creates a buildx builder that uses the mirror and trusts its CA

If you run `docker/setup-buildx-action` after this action, it will overwrite the buildx builder created by this action.

[Learn more](https://docs.actuated.com/tasks/registry-mirror/)

## Examples

The `v3` version uses TLS for the registry with a CA injected to the VM and is the same as `master`

```yaml
      - uses: self-actuated/hub-mirror@v3
```

Set a custom MTU for Docker's bridges:

```yaml
      - uses: self-actuated/hub-mirror@v4
        with:
          mtu: 1450
```

## License

[MIT License](./LICENSE)
