# templates

This repo contains aux files for different types of projects

* `app/` - an arbitrary golang application, with binary releases and docker image (ghcr.io only)
* `internal/` an arbitraty internal golang application, with docker image (ghcr.io and private registry)
* `cli/` - a golang CLI application, with binary releases
* `library/` - a golang library

```bash
find . -type f -exec sed -i 's|PROJECT|app-name|g' {} \;
# note: Dockerfile may need manual adjustment
```
