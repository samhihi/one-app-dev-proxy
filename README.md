<h1>
  <center>
    <br />
    <img src="./one-app-dev-proxy.png" alt="one-app-dev-proxy - One App" width="50%" />
    <br /><br />
  </center>
</h1>

> Proxy requests to remote servers locally while also allowing for an [express](https://expressjs.com) middleware to be provided and applied to all requests.


## 👩‍💻 Hiring 👨‍💻

Want to get paid for your contributions to `one-app-dev-proxy`?
> Send your resume to oneamex.careers@aexp.com


## 📖 Table of Contents

* [Features](#-features)
* [Usage](#-usage)
* [API](#-api)
* [Available Scripts](#-available-scripts)
* [contributing](#-contributing)

## ✨ Features

* Proxy requests to remote servers locally.
* Add an [express](https://expressjs.com) middleware applied to all requests.

## 🤹‍ Usage

### Installation

```bash
npm i @americanexpress/one-app-dev-proxy -D
```

Look at the different `options` you can use under the [API](#API) section.

```js
import oneAppDevProxy from '@americanexpress/one-app-dev-proxy';

  oneAppDevProxy({
    useMiddleware: true,
    pathToMiddleware: path.join(__dirname, '../../.dev/middleware'),
    remotes: { api: 'https://api.com' },
  })
```

## 🎛️ API

## oneAppDevProxy( [options] )

### options

Type: `object`

provide the options below to start the mock services.

#### useMiddleware

Type: `boolean`

Default: `false`<br>
provides the option of whether to apply provided middleware to `one-app-dev-proxy` server.

#### pathToMiddleware

Type: `string`
path to a file exporting an express middleware function by the HTTP_PROXY environment variable.

#### remotes

Type: `object`

Default: `{}`<br>
Configuration object containing paths `one-app-dev-proxy` should serve and where requests coming to those paths should be proxied to. Used if `pathToMiddleware` is not provided.

**Note**: one-app-dev-proxy respects the `HTTP_PROXY` / `http_proxy`,  `HTTPS_PROXY` / `https_proxy`,
and `NO_PROXY` / `no_proxy` environment variables and will use those accordingly when making
requests to remotes provided in the `remotes` option.

## 📜 Available Scripts

**`npm run build`**

Builds the module into the `build` folder.

**`npm test`**

Runs `eslint` **and** unit tests on the current branch.

## 🏆 Contributing

We welcome Your interest in the American Express Open Source Community on Github.
Any Contributor to any Open Source Project managed by the American Express Open
Source Community must accept and sign an Agreement indicating agreement to the
terms below. Except for the rights granted in this Agreement to American Express
and to recipients of software distributed by American Express, You reserve all
right, title, and interest, if any, in and to Your Contributions. Please [fill
out the Agreement](https://cla-assistant.io/americanexpress/one-app-dev-proxy).

Please feel free to open pull requests and see [CONTRIBUTING.md](./CONTRIBUTING.md) for commit formatting details.

## 🗝️ License

Any contributions made under this project will be governed by the [Apache License
2.0](https://github.com/americanexpress/one-app-dev-proxy/blob/master/LICENSE.txt).

## 🗣️ Code of Conduct

This project adheres to the [American Express Community Guidelines](https://github.com/americanexpress/one-app-dev-proxy/wiki/Code-of-Conduct).
By participating, you are expected to honor these guidelines.