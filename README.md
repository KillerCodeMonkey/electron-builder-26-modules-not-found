# electron-builer26-formdata

An Electron application with React and TypeScript build with electron-vite

Reproduction repo for https://github.com/electron-userland/electron-builder/issues/9006#issuecomment-2774697717


Installs and uses `form-data` package in `main.ts` and builds the app.

Build the AppImage with following command: `NPM_CONFIG_PRODUCTION=false NODE_ENV=production npm run build:linux`

Starting the AppImage results in:

```BASH
A JavaScript error occurred in the main process
Uncaught Exception:
Error: Cannot find module 'dunder-proto/get'
Require stack:
- /tmp/.mount_electrviD0TZ/resources/app.asar/node_modules/get-proto/index.js
- /tmp/.mount_electrviD0TZ/resources/app.asar/node_modules/get-intrinsic/index.js
- /tmp/.mount_electrviD0TZ/resources/app.asar/node_modules/es-set-tostringtag/index.js
- /tmp/.mount_electrviD0TZ/resources/app.asar/node_modules/form-data/lib/form_data.js
- /tmp/.mount_electrviD0TZ/resources/app.asar/out/main/index.js
-
    at Module._resolveFilename (node:internal/modules/cjs/loader:1232:15)
    at s._resolveFilename (node:electron/js2c/browser_init:2:129170)
    at Module._load (node:internal/modules/cjs/loader:1062:27)
    at c._load (node:electron/js2c/node_init:2:18008)
    at TracingChannel.traceSync (node:diagnostics_channel:322:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:227:24)
    at Module.require (node:internal/modules/cjs/loader:1318:12)
    at require (node:internal/modules/helpers:136:16)
    at Object.<anonymous> (/tmp/.mount_electrviD0TZ/resources/app.asar/node_modules/get-proto/index.js:6:22)
    at Module._compile (node:internal/modules/cjs/loader:1569:14)
```

But it is working with electron-builder v25.

## Recommended IDE Setup

- [VSCode](https://code.visualstudio.com/) + [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) + [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## Project Setup

### Install

```bash
$ npm install
```

### Development

```bash
$ npm run dev
```

### Build

```bash
# For windows
$ npm run build:win

# For macOS
$ npm run build:mac

# For Linux
$ npm run build:linux
```
