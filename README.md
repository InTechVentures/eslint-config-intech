# Intech Ventures ESLint Config

Based on [wesbos/eslint-config-wesbos], this repository defines the ESLint and Prettier rules at Intech Ventures

## Adding to a new project

1. To use this in a new project simply install everything you need using the following command (works with yarn):

```
npx install-peerdeps --dev eslint-config-intech
```

2. Add the following ESLint configuration to the project's package.json. `.eslintrc` and `.prettierrc` files can be safely removed from the project.

```
"eslintConfig": {
  "extends": [
    "eslint-config-intech"
  ]
}
```

## Usage with VSCode
- Install the VSCode [ESLint plugin](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- Since Prettier is automatically ran through ESLint, it does not have to be enabled in VSCode settings. Match your settings.json with this

```javascript
{
  "editor.formatOnSave": true,

  // Do not automatically format JavaScript or JavaScript react, as this will be done by ESLint
  "[javascript]": { "editor.formatOnSave": false },
  "[javascriptreact]": { "editor.formatOnSave": false },
  "[typescript]": { "editor.formatOnSave": false },
  "[typescriptreact]": { "editor.formatOnSave": false },

  // Run ESLint on Save
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },

  "prettier.disableLanguages": ["javascript", "javascriptreact", "typescript", "typescriptreact"]
}

```
