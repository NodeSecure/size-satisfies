# `size-satisfies`
![version](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/NodeSecure/size-satisfies/master/package.json&query=$.version&label=Version)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/NodeSecure/size-satisfies/commit-activity)
![MIT](https://img.shields.io/github/license/mashape/apistatus.svg)
![dep](https://img.shields.io/david/NodeSecure/size-satisfies)
![size](https://img.shields.io/github/languages/code-size/NodeSecure/size-satisfies)

Same as SemVer.satisfies but for file size!

## Requirements
- [Node.js](https://nodejs.org/en/) v12 or higher

## Getting Started

This package is available in the Node Package Repository and can be easily installed with [npm](https://docs.npmjs.com/getting-started/what-is-npm) or [yarn](https://yarnpkg.com).

```bash
$ npm i @nodesecure/size-satisfies
# or
$ yarn add @nodesecure/size-satisfies
```

## Usage example

```js
import { strict } from "assert";
import sizeSatisfies from "size-satisfies";

const { strictEqual } = strict;

strictEqual(sizeSatisfies(">= 45KB", "20MB"), true);
strictEqual(sizeSatisfies("= 1MB", "1MB"), true);
strictEqual(sizeSatisfies("= 1MB", 2000), false);
```

The first argument of the `sizeSatisfies` method is the pattern with the operator + size. Available operators are `>=`, `<=`, `>`, `<`, `=`.

## API

### sizeSatisfies(pattern: string, size: number | string): boolean
When the size is a string we convert it to a bytes number. When the argument is a number we consider the value as bytes.

Invalid pattern will always return **false**.


## Contributors ✨

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-3-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://www.linkedin.com/in/thomas-gentilhomme/"><img src="https://avatars.githubusercontent.com/u/4438263?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Gentilhomme</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=fraxken" title="Code">💻</a> <a href="https://github.com/NodeSecure/size-satisfies/commits?author=fraxken" title="Documentation">📖</a> <a href="https://github.com/NodeSecure/size-satisfies/pulls?q=is%3Apr+reviewed-by%3Afraxken" title="Reviewed Pull Requests">👀</a> <a href="#security-fraxken" title="Security">🛡️</a> <a href="https://github.com/NodeSecure/size-satisfies/issues?q=author%3Afraxken" title="Bug reports">🐛</a></td>
    <td align="center"><a href="https://github.com/Rossb0b"><img src="https://avatars.githubusercontent.com/u/39910164?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Nicolas Hallaert</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=Rossb0b" title="Documentation">📖</a></td>
    <td align="center"><a href="http://tonygo.dev"><img src="https://avatars.githubusercontent.com/u/22824417?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Tony Gorez</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=tony-go" title="Code">💻</a> <a href="https://github.com/NodeSecure/size-satisfies/commits?author=tony-go" title="Documentation">📖</a> <a href="https://github.com/NodeSecure/size-satisfies/pulls?q=is%3Apr+reviewed-by%3Atony-go" title="Reviewed Pull Requests">👀</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

## License
MIT
