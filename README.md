# Jest-Test
Demo Repository for [Jest Issue #5736](https://github.com/facebook/jest/issues/5736)

## How to

1. run `npm i`
1. run `npm test`
1. see error `TypeError: Cannot read property 'loose' of undefined (While processing preset: "/Users/x/Desktop/jest-test/node_modules/babel-preset-react-app/index.js")`

## Further

I've searched for this error and found [this Babel issue](https://github.com/babel/babel/issues/7110#issuecomment-354948931), that suggests that when `babel-core` instead of `@babel/core` is required by any package, it will break. And it seems like `jest-runtime` v22.4.2 (currently the newest one) is doing exactly this.

## System

* **Operating System**: MacOS 10.13.2 (High Sierra)
* **Nodejs**: v9.4.0
* **npm**: v5.7.1
