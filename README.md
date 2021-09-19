# ESLint + Prettier Config for React (Next.js)

`eslint-config-fnxl`

> A config for ESLint and Prettier, to be used with Next.js React Projects.

My first package published to NPM

## Overview

This config extends the famous [airbnb](https://www.npmjs.com/package/eslint-config-airbnb) ESLint config and Prettier integration via the ESLint plugin.
A few rules are overriden for a more relaxed development experience in Next.js applications out of the box.

The goal of this configuration is to get code linting and formatting up and running as quickly as possible without having to configure ESLint + Prettier from scratch everytime for each new project.

## Installation

To install this config you need to have `npm verion > 7.0.0`

```
npm install -D eslint-config-fnxl
```

This will install this ocnfig as well as its peer dependencies:

- eslint
- eslint-config-airbnb
- eslint-plugin-import
- eslint-plugin-jsx-a11y
- eslint-config-prettier
- eslint-plugin-prettier
- eslint-plugin-react
- eslint-plugin-react-hooks
- prettier

**NOTE**: if you are on older version of npm (<7.0.0), you will need to install these manually.

```
npx install-peerdeps -D eslint-config-fnxl
```

## Usage

To start using this config, extend this config in your `.eslintrc` file

```
//.eslintrc
{
  "extends": ["fnx"]
}
```

Additionally, you can override rules and configure your personal linting rules in this file to your heart's content.

## Prettier

This config supports prettier integration out of the box. Rules that may conflict with ESLint are disabled.

If you wish to override any prettier options, you can do so by specifying them under `prettier/prettier` rule in your ESLint config file.

```
// .eslintrc
{
  "extends": ["fnx"],
  "rules": {
    "prettier/prettier" : [
      "error",
      {
        "printWidth": 110
      }
    ]
  }
}
```

Make sure that these rules match the options specified in your `.prettierrc` file

## License

Lincensed under MIT License.
