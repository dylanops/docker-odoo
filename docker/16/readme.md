# Build image with multi arch

```bash

export DOCKER_USER=dylanops

docker buildx build -t "${DOCKER_USER}/odoo:16.0" --platform linux/amd64,linux/arm64 --push .

docker buildx imagetools inspect "$DOCKER_USER/odoo:16.0"

docker run --rm "$DOCKER_USER/odoo:16.0"

```