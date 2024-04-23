# hub-mirror

GitHub Action to configure a Docker Hub mirror for actuated servers.

Warning, running `docker/setup-buildx-action` after this step will wipe out the configuration set by this action.

```yaml
      - uses: self-actuated/hub-mirror@master
```

Or pin to a version:

```yaml
      - uses: self-actuated/hub-mirror@v2
```
