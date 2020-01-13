
![RiSE Logo][logo]

# RiSE JavaScript/TypeScript SDK Sockets

[![NPM version][npm-image]][npm-url]
[![Build Status][ci-image]][ci-url]
[![Dependency Status][daviddm-image]][daviddm-url]

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)

This is the Default Sockets library for `@rise/sdk-js`

# Installation

```
npm install @rise/sdk-js-sockets --save
```

# Usage

### Getting started
When initiating your RiSE instance, inject the sockets

```js
// Create a new instance
import sockets from '@rise/sdk-js-sockets'
const rise = new RiSE({
  sandbox: true,
  public_key: <public_key>,
  private_key: <private_key>,
  sockets: sockets
})

// Authenticate for later requests by the API
rise.authenticateApiUser(
  <channel_uuid>,
  <adminIdentifier>,
  <adminPassword>
)
  .then(res => {
    <adminToken> = res.token
    adminSession = res.session
  })
  .catch(err => console.log)
})

```
## Setup

# Documentation
A quick start documentation, see the full documentation here.
 
## Contributing

### Release Instructions
When the master is tagged with a release, it will automatically publish to npm, updates the Changelog and bumps the version. The SDK uses the [standard-version library](https://www.npmjs.com/package/standard-version) to manage it all.

To run a patch release: 
```bash
npm run release -- --release-as patch
``` 
and then commit to master. `git push --follow-tags origin master`

You can also test the release by running
```bash
npm run release -- --dry-run --release-as patch
``` 
 
[logo]: https://rise.store/wp-content/uploads/2019/06/rise_sized_75x150_blk-01-01-01.png "RiSE"
[npm-image]: https://img.shields.io/npm/v/@rise/sdk-js-sockets.svg?style=flat-square
[npm-url]: https://npmjs.org/package/@rise/sdk-js-sockets
[ci-image]: https://img.shields.io/circleci/project/github/rise-app/rise-sdk-js-sockets/master.svg
[ci-url]: https://circleci.com/gh/rise-app/rise-sdk-js-sockets/tree/master
[daviddm-image]: http://img.shields.io/david/rise-app/rise-sdk-js-sockets.svg?style=flat-square
[daviddm-url]: https://david-dm.org/rise-app/rise-sdk-js-sockets
[coverage-image]: https://img.shields.io/codeclimate/coverage/github/rise-app/rise-sdk-js-sockets.svg?style=flat-square
[coverage-url]: https://codeclimate.com/github/rise-app/rise-sdk-js-sockets/coverage
