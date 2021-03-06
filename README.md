# remotely

## Table of Contents

- [Prerequisites](#prerequisites)
- [Install](#install)
- [Usage](#usage)
- [Config](#config)
- [Maintainers](#maintainers)
- [Contribute](#contribute)
- [License](#license)

## Prerequisites
- rsync

## Install
```
npm install -g https://github.com/charlesbodman/remotely
```

## Usage

**Create remotely config (`.remotely.json`)**
```
$ remotely init
```
Run this in any parent directory from where you are going to be running `remotely`.

Remotely will climb up and use the first config file it finds
[Read about config here](#config)

Make sure you edit your config (`.remotely.json`) file after doing this.

---

**Watch local directory for changes and rsync push on change**
```
$ remotely watch
```
---

**Rsync pull down remote**
```
$ remotely pull
```
---

**Rsync push to remote**
```
$ remotely push
```
---

## Config
Remotely will look for the config file `.remotely.json` in any directory above where you call `remotely [command]`.
This means that the config can belong anywhere, as long as remotely can find it by traversing upwards

| Config        | Desc         |                |
| ------------- |:-------------:|:-------------:|
| local         | local path to sync dir | required |
| remote      | remote host and path | required |
| rsync_flags | flags to customize rsync  | optional |
| dry_run | perform dry run | optional |
| exclude | files or directories to exclude | optional |

**Example config**

This could live in `/Users/charliebodman/documents/kano/apps/.remotely.json`
You can create remotely config by calling `remotely init`
```javascript
{
    "local":"/Users/charliebodman/documents/kano/apps",
    "remote":"charlie@example.com:~/kano/apps"
}
```

## Maintainers

[@charlesbodman](https://github.com/@charlesbodman)

## Contribute

PRs accepted.

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

MIT © 2017 Charles Bodman
