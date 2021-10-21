This action allow you to install and lint your JS file and get only compiled files (run it on node:10.x, 12.x, 14.x, latest)

You need to replace the inputs commands:

```
      - name: building
        uses: PrestaShopCorp/github-action-lint-js/{version}@master
        with:
          cmd: npm | yarn
          path: $PATH | you can leave it blank if the project and has the root
```
