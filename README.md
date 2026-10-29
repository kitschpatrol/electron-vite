<!-- title -->

# @kitschpatrol/electron-vite

<!-- /title -->

<!-- badges -->

[![NPM Package @kitschpatrol/electron-vite](https://img.shields.io/npm/v/@kitschpatrol/electron-vite.svg)](https://npmjs.com/package/@kitschpatrol/electron-vite)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/license/mit/)
[![CI](https://github.com/kitschpatrol/electron-vite/actions/workflows/ci.yml/badge.svg)](https://github.com/kitschpatrol/electron-vite/actions/workflows/ci.yml)

<!-- /badges -->

<!-- short-description -->

**Fork of electron-vite with hotfixes.**

<!-- /short-description -->

This is a fork of [alex8088/electron-vite](https://github.com/alex8088/electron-vite).

Currently, it matches the upstream version except for one hotfix: the Electron binary is downloaded on first launch (Electron 42+ no longer downloads it during install), and Electron 45 has its own build targets. It is published to npm as [`@kitschpatrol/electron-vite`](https://www.npmjs.com/package/@kitschpatrol/electron-vite).

I originally forked to incorproate patches from [desirecore/electron-vite](https://github.com/desirecore/electron-vite).

The original readme follows with light modifications:

---

<p align="center">
  <img src="https://alex8088.github.io/assets/electron-vite.svg" width="150px" height="150px">
</p>

<div align="center">
  <h1>electron-vite</h1>
</div> <p align="center">Next generation Electron build tooling based on Vite</p>

<p align="center">
<a href="https://electron-vite.org">Documentation</a> |
<a href="https://electron-vite.org/guide">Getting Started</a> |
<a href="https://github.com/alex8088/quick-start/tree/master/packages/create-electron">create-electron</a>
</p>

<p align="center">
<a href="https://cn.electron-vite.org">中文文档</a>
</p>

<br /> <br />

## Features

- ⚡️ [Vite](https://vitejs.dev) powered and use the same way.
- 🛠 Pre-configure with sensible defaults optimized for Electron.
- 💡 Optimize asset handling for Electron main process.
- 🚀 Fast HMR & hot reloading.
- 🔥 Isolated build for multi-entry application development.
- ✨ Simplify multi-threading development.
- 🔒 Compile code to v8 bytecode to protect source code.
- 🔌 Easy to debug in IDEs such as VSCode or WebStorm.
- 📦 Out-of-the-box support for TypeScript, Vue, React, Svelte, SolidJS and more.

## Usage

### Install

> This is a community fork published as [`@kitschpatrol/electron-vite`](https://www.npmjs.com/package/@kitschpatrol/electron-vite). The CLI command remains `electron-vite`.

```sh
npm i @kitschpatrol/electron-vite -D
```

### Development & Build

In a project where `electron-vite` is installed, you can use `electron-vite` binary directly with `npx electron-vite` or add the npm scripts to your `package.json` file like this:

```json
{
  "scripts": {
    "start": "electron-vite preview",
    "dev": "electron-vite dev",
    "prebuild": "electron-vite build"
  }
}
```

### Configuration

When running `electron-vite` from the command line, electron-vite will automatically try to resolve a config file named `electron.vite.config.js` inside project root. The most basic config file looks like this:

```js
// electron.vite.config.js
export default {
  main: {
    // vite config options
  },
  preload: {
    // vite config options
  },
  renderer: {
    // vite config options
  }
}
```

### Getting Started

Clone the [electron-vite-boilerplate](https://github.com/alex8088/electron-vite-boilerplate) or use the [create-electron](https://github.com/alex8088/quick-start/tree/master/packages/create-electron) tool to scaffold your project.

```bash
npm create @quick-start/electron@latest
```

Currently supported template presets include:

|                                                 JavaScript                                                 |                                                    TypeScript                                                    |
| :--------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------: |
| [vanilla](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/vanilla) | [vanilla-ts](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/vanilla-ts) |
|     [vue](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/vue)     |     [vue-ts](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/vue-ts)     |
|   [react](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/react)   |   [react-ts](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/react-ts)   |
|  [svelte](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/svelte)  |  [svelte-ts](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/svelte-ts)  |
|   [solid](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/solid)   |   [solid-ts](https://github.com/alex8088/quick-start/tree/master/packages/create-electron/playground/solid-ts)   |

## Contribution

See [Contributing Guide](CONTRIBUTING.md).

## License

[MIT](./LICENSE) © alex.wei
