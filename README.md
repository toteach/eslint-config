# Eslint config by toteach.io

> Programs must be written for people to read, and only incidentally for machines to execute. 
> ###### Harold Abelson

#### Content:
- [⚙ Eslint config integration](#eslint-config-integration)
- [◉ Eslint config options](#eslint-config-options)


## Eslint config integration

First, what you need is to install npm package.
```bash
npm install --save-dev @toteach/eslint-config
```

Next, install all peer dependencies. The easiest way is to add this lines to your `devDependensies`
```json
{
  "eslint": "^6.6.0",
  "@typescript-eslint/parser": "^2.9.0",
  "eslint-plugin-import": "^2.18.2",
  "eslint-plugin-simple-import-sort": "^4.0.0",
  "eslint-plugin-vue": "^6.0.0",
  "@typescript-eslint/eslint-plugin": "^2.6.1",
  "@vue/eslint-config-typescript": "^4.0.0",
  "vue-eslint-parser": "^7.0.0",
  "typescript": "^3.6.4",
  "babel-eslint": "^10.0.3"
}
```

After previous operations add this to your eslint configuration.
```json
{
  "extends": [
    "@toteach/eslint-config"
  ],
  "parserOptions": {
    "project": "./tsconfig.json",
    "sourceType": "module",
    "extraFileExtensions": [".vue"]
  }
}
```
**PROFIT!** Now you can use our eslint configuration in your awesome projects!

> Minimal eslint configuration example 
```json
{
  "root": true,
  "parserOptions": {
    "project": "./tsconfig.json",
    "sourceType": "module",
    "extraFileExtensions": [".vue"]
  },
  "extends": [
    "@toteach/eslint-config"
  ]
}
```

[⬆ Go top](#eslint-config-by-toteachio)

---

## Eslint config options

### Here we have 3 configs:

#### base
- vue linting
- typescript
- javascript linting

Usage:
```json
{
  "extends": ["@toteach/eslint-config"]
}
```

> Also, If you have typescript and javascript `.vue` files. You can change the extension from `.vue` to `.js.vue`. Linter will check code in these components like a javascript.


#### vue javascript only
> Combined `vue-html` and `javascript` rules

Usage:
```json
{
  "extends": ["@toteach/eslint-config/vue-javascript"]
}
```

#### only vue html
Usage:
```json
{
  "extends": ["@toteach/eslint-config/vue-html"]
}
```

#### only typescript
Usage:
```json
{
  "extends": ["@toteach/eslint-config/typescript"]
}
```

#### only javascript
Usage:
```json
{
  "extends": ["@toteach/eslint-config/javascript"]
}
```

[⬆ Go top](#eslint-config-by-toteachio)
