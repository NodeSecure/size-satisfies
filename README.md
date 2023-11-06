# `size-satisfies`

![version](https://img.shields.io/badge/dynamic/json.svg?style=for-the-badge&url=https://raw.githubusercontent.com/NodeSecure/size-satisfies/master/package.json&query=$.version&label=Version)
[![OpenSSF
Scorecard](https://api.securityscorecards.dev/projects/github.com/NodeSecure/size-satisfies/badge?style=for-the-badge)](https://api.securityscorecards.dev/projects/github.com/NodeSecure/size-satisfies)
![MIT](https://img.shields.io/github/license/NodeSecure/size-satisfies.svg?style=for-the-badge)
![size](https://img.shields.io/github/languages/code-size/NodeSecure/size-satisfies?style=for-the-badge)
![build](https://img.shields.io/github/actions/workflow/status/NodeSecure/size-satisfies/node.js.yml?style=for-the-badge)

Same as SemVer.satisfies but for file size!

## Requirements

- [Node.js](https://nodejs.org/en/) v18 or higher

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

[![All Contributors](https://img.shields.io/badge/all_contributors-6-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://www.linkedin.com/in/thomas-gentilhomme/"><img src="https://avatars.githubusercontent.com/u/4438263?v=4?s=100" width="100px;" alt="Gentilhomme"/><br /><sub><b>Gentilhomme</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=fraxken" title="Code">💻</a> <a href="https://github.com/NodeSecure/size-satisfies/commits?author=fraxken" title="Documentation">📖</a> <a href="https://github.com/NodeSecure/size-satisfies/pulls?q=is%3Apr+reviewed-by%3Afraxken" title="Reviewed Pull Requests">👀</a> <a href="#security-fraxken" title="Security">🛡️</a> <a href="https://github.com/NodeSecure/size-satisfies/issues?q=author%3Afraxken" title="Bug reports">🐛</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/Rossb0b"><img src="https://avatars.githubusercontent.com/u/39910164?v=4?s=100" width="100px;" alt="Nicolas Hallaert"/><br /><sub><b>Nicolas Hallaert</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=Rossb0b" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="http://tonygo.dev"><img src="https://avatars.githubusercontent.com/u/22824417?v=4?s=100" width="100px;" alt="Tony Gorez"/><br /><sub><b>Tony Gorez</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=tony-go" title="Code">💻</a> <a href="https://github.com/NodeSecure/size-satisfies/commits?author=tony-go" title="Documentation">📖</a> <a href="https://github.com/NodeSecure/size-satisfies/pulls?q=is%3Apr+reviewed-by%3Atony-go" title="Reviewed Pull Requests">👀</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/tekeuange23"><img src="https://avatars.githubusercontent.com/u/35274201?v=4?s=100" width="100px;" alt="tekeuange23"/><br /><sub><b>tekeuange23</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=tekeuange23" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/fabnguess"><img src="https://avatars.githubusercontent.com/u/72697416?v=4?s=100" width="100px;" alt="Kouadio Fabrice Nguessan"/><br /><sub><b>Kouadio Fabrice Nguessan</b></sub></a><br /><a href="#maintenance-fabnguess" title="Maintenance">🚧</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/clbcky"><img src="https://avatars.githubusercontent.com/u/113340767?v=4?s=100" width="100px;" alt="clbcky"/><br /><sub><b>clbcky</b></sub></a><br /><a href="https://github.com/NodeSecure/size-satisfies/commits?author=clbcky" title="Tests">⚠️</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

## License

MIT
