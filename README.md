# Standard ESLint for React Zero41 Projects

## Installation

1. Install `eslint`:
  ```sh
  yarn add eslint^8 --dev
  ```
  ```sh
  npm i eslint@^8 --save-dev
  ```
  
2. Install `eslint-config-zero41-react`:
  ```sh
  yarn add esling-config-zero41@https://github.com/Zero41/eslint-config-zero41-react.git --dev
   ```
  ```sh
  npm install eslint-config-zero41-react@github:Zero41/eslint-config-zero41-react --save-dev
  ```

3. Add `eslint-config-zero41-react` to your ESLint `.eslintrc.js` config:
  ```javascript
  module.exports = {
    root: true,
    extends: ["eslint-config-zero41-react"],
    parserOptions: {
      project: "./tsconfig.json",
      tsconfigRootDir: __dirname,
    },
  };
  ```

4. If you are using absolute imports, use paths to define the root:
  ```diff
  module.exports = {
    root: true,
    extends: ["eslint-config-zero41-react"],
  +  settings: {
  +    "import/resolver": {
  +      node: {
  +        paths: ["./"],
  +      },
  +    },
  + },
    parserOptions: {
      project: "./tsconfig.json",
      tsconfigRootDir: __dirname,
    },
  };
  ```
  
5. If you have files types other than `*.js`, `*.jsx`, `*.ts` or `*.tsx` add them:
  ```diff
  module.exports = {
    root: true,
    extends: ["eslint-config-zero41-react"],
    settings: {
      "import/resolver": {
        node: {
          paths: ["./"],
  +         extensions: [".js", ".jsx", ".ts", ".tsx", ".mjs"],
        },
      },
    },
    parserOptions: {
      project: "./tsconfig.json",
      tsconfigRootDir: __dirname,
    },
  };
  ```
## Other ESLint Configs
- Standard ESLint for Zero41 Projects: [eslint-config-zero41](https://github.com/Zero41/eslint-config-zero41)
- Standard ESLint for React Native Zero41 Projects: [eslint-config-zero41-react-native](https://github.com/Zero41/eslint-config-zero41-react-native)
