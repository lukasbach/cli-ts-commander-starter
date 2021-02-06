# CLI Typescript Commander Starter

![Pretty](https://github.com/lukasbach/cli-ts-commander-starter/workflows/Pretty/badge.svg)
![Testing](https://github.com/lukasbach/cli-ts-commander-starter/workflows/Testing/badge.svg)
![Publish](https://github.com/lukasbach/cli-ts-commander-starter/workflows/Publish/badge.svg)

A template repository for CLI tools based on Typescript and CommanderJs. Features

- Test setup with AVA
- Prettier setup
- Setup with Yarn
- Commander code template that automatically reads the version from the package.json file
- Dev `yarn start` command with `ts-node`
- Bundles native executables with `pkg` for Windows, Mac OS and linux
- Github Actions CI Pipeline that
  - builds app and runs tests
  - checks prettier
  - bundles app into native binaries and deploys them as a GitHub release
  - deploys the package to NPM

Example repo: https://github.com/lukasbach/json-extract-path

## Setup template

- Clone the template via the _Use this template_ button or by clicking
  [here](https://github.com/lukasbach/cli-ts-commander-starter/generate).
- Add a secret to GitHub with the name `npm_token` to allow NPM releases
- Push tags with the format `v0.0.0` to automatically publish new releases.

## How to use

Install globally via

    npm install -g {TOOLNAME}

or directly use via

    npx {TOOLNAME}

You can also [download a prebuilt binary](https://github.com/lukasbach/cli-ts-commander-starter/releases) and run that.

Usage:

    Usage: npx {TOOLNAME} [options]

    Options:
    -V, --version            output the version number
    -s, --small              small pizza size
    -p, --pizza-type <type>  flavour of pizza
    -h, --help               display help for command

## How to develop

- `yarn` to install dependencies
- `yarn start` to run the CLI script for debugging
- `yarn test` to run tests
- `yarn prettier:check` to verify that your code is pretty
- `yarn prettier:write` to make your code pretty

Don't manually publish the package to NPM! You can just tag
a commit with a new release tag (remember to bump the version
in `package.json`) and push the changes, a Github Action
will deploy the new version to NPM.
