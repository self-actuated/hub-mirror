# hub-mirror

GitHub Action to configure a Docker Hub mirror for actuated servers.

[Learn more](https://docs.actuated.com/tasks/registry-mirror/)

Warning: running `docker/setup-buildx-action` after this step will wipe out the configuration set by this action. You do not need to use `docker/setup-buildx-action` when you use this action.

```yaml
      - uses: self-actuated/hub-mirror@master
```

The `v3` version uses TLS for the registry with a CA injected to the VM and is the same as `master`

```yaml
      - uses: self-actuated/hub-mirror@v3
```

The `v2` version was prior to using TLS for the registry, using HTTP and `insecure`:

```yaml
      - uses: self-actuated/hub-mirror@v2
```
