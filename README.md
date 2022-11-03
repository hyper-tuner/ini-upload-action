# HyperTuner INI upload

GitHub Action for INI upload.

## Usage

`.github/workflows/upload-ini.yml`

```yaml
name: Upload INI

on: pull_request

jobs:
  upload:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Upload INI
        uses: hyper-tuner/ini-upload-action@v1
        with:
          api-url: "https://api.hypertuner.cloud"
          username: "admin-uploader@example.com"
          password: "danger-to-manifold"
          path: "path/to.ini"
          ecosystem: "speeduino"
```
