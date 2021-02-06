# CLI Typescript Commander Starter

A template repository for CLI tools based on Typescript and CommanderJs. Features

- Test setup with AVA
- Prettier setup
- Setup with Yarn
- Commander code template that automatically reads the version from the package.json file
- Dev ``yarn start`` command with ``ts-node``
- Bundles native executables with ``pkg`` for Windows, Mac OS and linux
- Github Actions CI Pipeline that
  - builds app and runs tests
  - checks prettier
  - bundles app into native binaries and deploys them as a GitHub release
    
## How to use

Install globally via

    npm install -g {TOOLNAME}

or directly use via

    npx {TOOLNAME}

Usage:

    Usage: npx {TOOLNAME} [options]

    Options:
    -V, --version            output the version number
    -s, --small              small pizza size
    -p, --pizza-type <type>  flavour of pizza
    -h, --help               display help for command

## How to develop

- ``yarn`` to install dependencies
- ``yarn start`` to run the CLI script for debugging
- ``yarn test`` to run tests
- ``yarn publish`` to publish a new version to NPM. Make sure to bump the version!
- ``yarn prettier:check`` to verify that your code is pretty
- ``yarn prettier:write`` to make your code pretty