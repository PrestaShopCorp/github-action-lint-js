# GitHub Action : Lint JS

This action allow you to install your dependencies and lint your JS files (run it on node:10.x, 12.x, latest)

## Pre-requesites

An script `lint` must be defined in the package.json of the target project.

Example:

```json
{
  [...]
  "scripts": {
    "lint": "vue-cli-service lint"
  }
}
```

## How to run this action

You need to replace the inputs commands:

```yaml
      - name: Lint JS files
        uses: PrestaShopCorp/github-action-lint-js/{version}@v1.0
        with:
          cmd: npm | yarn
          path: $PATH (Optional: you can leave it blank if the JS project is stored in the root directory)
```

Versions available are stored in the subfolders of this repository.

Example:

```yaml
      - name: Lint JS files
        uses: PrestaShopCorp/github-action-lint-js/12@v1.0
        with:
          cmd: npm
          path: _dev
```