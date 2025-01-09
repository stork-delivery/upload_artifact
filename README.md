# Stork Upload Artifact To Version Action

This action uploads an artifact to a version in the Stork platform.

```yaml
jobs:
  build_linux:
    name: Build and Upload
    runs-on: ubuntu-latest

    steps:
    # Other steps to build ...
    - uses: stork-delivery/upload_artifact@main
        with:
          version: ${{ github.ref_name }}
          app-id: ${{ secrets.STORK_APP_ID }}
          api-key: ${{ secrets.STORK_API_KEY }}
          platform: linux # or windows, or macos, or whatever 
          artifact-path: path/to/the/artifact

```
