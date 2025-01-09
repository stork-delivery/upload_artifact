# Stork Upload Artifact To Version Action

This action uploads an artifact to a version in the Stork platform.

```yaml
jobs:
  create_version:
    name: Create Stork Version
    runs-on: ubuntu-latest

    steps:
      - uses: stork-delivery/create_version@main
        with:
          version: ${{ github.ref }}
          app-id: ${{ secrets.STORK_APP_ID }}
          api-key: ${{ secrets.STORK_API_KEY }}
```
