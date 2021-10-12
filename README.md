To reproduce the bug

- `git clone` the repo
- make sure you have rush installed globally, or use npx
- `rush update`
- `cd packages/trunk-package`
- `rush add -p leaf-package`
- `rush build` <- Will fail

Work around:
- `rm common/config/rush/npm-shrinkwrap.json`
- `rush update && rush build`
