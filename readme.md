# Intech Ventures ESLint Config

Based on [wesbos/eslint-config-wesbos], this repository defines the ESLint and Prettier rules at Intech Ventures

## Adding to a new project

To use this in a new project simply install everything you need using the following

```
npx install-peerdeps --dev eslint-config-intech
```

add the following ESLint configuration to the project's package.json

```
"eslintConfig": {
  "extends": [
    "eslint-config-intech"
  ]
}
```
