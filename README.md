This is this repo https://github.com/ben-rogerson/twin.examples/tree/master/component-library-styled-components with Storybook at the root. I've changed Button.tsx slightly in /packages/shared-ui/components to use a custom property from tailwind.config.js at the root of the project.

Currently, running `yarn && yarn build && yarn dev` works as expected.

When running `yarn storybook`, the custom property is not found.

When changing the root's package.json config from 
```
"babelMacros": {
    "twin": {
      "config": "./../../tailwind.config.js",
      "preset": "styled-components"
    }
  },
  ```
  to
  ```
"babelMacros": {
    "twin": {
      "config": "tailwind.config.js",
      "preset": "styled-components"
    }
  },
  ```
  Storybook works but running `yarn && yarn build && yarn dev` does not. The custom propery is not found.