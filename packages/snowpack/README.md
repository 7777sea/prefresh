# Prefresh-snowpack

[![npm version](https://badgen.net/npm/v/@prefresh/snowpack)](https://www.npmjs.com/package/@prefresh/snowpack)

## Setup

If you're using the [`preact-template`](https://github.com/pikapkg/create-snowpack-app/tree/master/packages/app-scripts-preact) you'll get this behavior
out of the box, if you don't or are using the old version fo it you'll have to follow these instructions.

```
npm i -s @prefresh/snowpack
## OR
yarn add @prefresh/snowpack
```

You'll have to add a few things, as seen in [this PR](https://github.com/pikapkg/create-snowpack-app/pull/54/files).

Add `react-refresh/babel` to your `babel.config.json`:

```json
{
  "presets": [["@babel/preset-react", {
    "pragma": "h",
    "pragmaFrag": "Fragment"
  }], "@babel/preset-typescript"],
  "plugins": ["@babel/plugin-syntax-import-meta", "react-refresh/babel"]
}
```

After adding it to your `babel-config` you'll have to make sure your `snowpack.config.json` contains both `plugin-babel` and `@prefresh/snowpack`

```json
{
  "plugins": [
    "@snowpack/plugin-babel",
    "@prefresh/snowpack"
  ]
}
```
