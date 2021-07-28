# Flow-to-TypeScript 

[build]: https://img.shields.io/circleci/project/bcherny/flow-to-typescript.svg?branch=master&style=flat-square
[npm]: https://img.shields.io/npm/v/flow-to-typescript.svg?style=flat-square
[mit]: https://img.shields.io/npm/l/flow-to-typescript.svg?style=flat-square

> Compile Flow files to TypeScript

**In Pre-Alpha - contributions welcome.**

## Installation

```sh
# Using Yarn:
yarn add flow-to-typescript

# Or, using NPM:
npm install flow-to-typescript --save
```

## Usage

### CLI

```sh
# Install globally
yarn global add flow-to-typescript

# Compile a file (all of these are equivalent)
flow2ts my/file.js.flow
flow2ts my/file.js.flow my/file.ts
flow2ts my/file.js.flow > my/file.ts
flow2ts -i my/file.js.flow -o my/file.ts
flow2ts --input my/file.js.flow --output my/file.ts
```

### Programmatic

```js
import { compile } from 'flow-to-typescript'
import { readFileSync, writeFileSync } from 'fs'

let path = 'path/to/file.js.flow'
let file = readFileSync(path, 'utf-8')

compile(file, path).then(ts =>
  writeFileSync('path/to/file.ts', ts)
)
```

## TypeScript vs. Flow
