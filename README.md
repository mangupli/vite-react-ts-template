# Vite bundle template

## React + Typescript + ESLint + Prettier

A modern, fast React project builder in Typescript with ESLint and Prettier presets.

## How to start

```
npx degit mangupli/vite-react-ts-template my-app

cd my-app

npm i
```

## `settings.json`

To customize formatting and linting on save, you need to write the following settings in `settings.json` (ctrl + shift + P):

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

You can add Prettier formatting for JS and React:

```json
{
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
```

When working from a directory other than the root directory, you must configure CWD for ESLint:

```json
{
  "eslint.workingDirectories": [
    { "directory": "./client", "changeProcessCWD": true },
    { "directory": "./server", "changeProcessCWD": true }
  ]
}
```

If the directory is not `client` or `server`, you can add the appropriate line to this array.
