qqjs
====

A bunch of wrappers for various utilites. Ideal for writing shell scripts in node. Everything here runs in synchronous mode for ease of use.

[![Version](https://img.shields.io/npm/v/qqjs.svg)](https://npmjs.org/package/qqjs)
[![CircleCI](https://circleci.com/gh/jdxcode/qqjs/tree/master.svg?style=svg)](https://circleci.com/gh/jdxcode/qqjs/tree/master)
[![Appveyor CI](https://ci.appveyor.com/api/projects/status/github/jdxcode/qqjs?branch=master&svg=true)](https://ci.appveyor.com/project/heroku/qqjs/branch/master)
[![Codecov](https://codecov.io/gh/jdxcode/qqjs/branch/master/graph/badge.svg)](https://codecov.io/gh/jdxcode/qqjs)
[![Greenkeeper](https://badges.greenkeeper.io/jdxcode/qqjs.svg)](https://greenkeeper.io/)
[![Known Vulnerabilities](https://snyk.io/test/npm/qqjs/badge.svg)](https://snyk.io/test/npm/qqjs)
[![Downloads/week](https://img.shields.io/npm/dw/qqjs.svg)](https://npmjs.org/package/qqjs)
[![License](https://img.shields.io/npm/l/qqjs.svg)](https://github.com/jdxcode/qqjs/blob/master/package.json)

Usage
=====

It's best to [look at the code](src/index.ts) to see what all is available, but here is an example of using it:

```js
const qq = require('qqjs')

// silent mode, otherwise it logs out every command
// qq.config.silent = true

// run a command with qq.x this runs synchronously using execa
// by default it will echo out to the screen the commmand, stdout/stderr and connect to stdin
// can send either a string
qq.x('git --version')

// or specify the arguments
qq.x('git' ['--version'])

qq.cd('newdir')

qq.cp('from', 'to')

const pjson = qq.readJSON('package.json')
qq.writeJSON('package.json', {})

// for almost any command, if it takes a string you can also pass an array and it will automatically path.join()
qq.writeJSON(['mydir', 'package.json'], {})
```

Status
======

- [x] x (exec)
- [x] readJSON
- [x] writeJSON
- [x] path
- [x] mkdirp
- [x] env
- [x] globby
- [x] read file
- [x] write file
- [x] cd
- [x] ls
- [x] cp (use cpy)
- [x] mv
- [x] rm
- [x] cwd
- [x] file exists
- [x] homedir
- [ ] ln
- [ ] is file/directory/symlink/etc
- [ ] chmod
- [ ] batch rename
- [ ] sed
- [ ] download files
- [ ] upload files
- [ ] aws s3
- [ ] resolve-from
- [ ] open-editor
- [ ] hasha
- [ ] temp files/dirs
- [ ] git stuff?
- [ ] find-up
- [ ] read-pkg
- [ ] which
- [ ] pushd/popd
