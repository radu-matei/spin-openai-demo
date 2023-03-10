# Spin and OpenAI

This is a sample Spin application written in TypeScript that uses the OpenAI
JavaScript client library to communicate with OpenAI.

![Demo](./demo.gif)

### Running from GitHub

```
$ spin up -f spin up -f ghcr.io/radu-matei/spin-openai-demo:v1
  api: http://127.0.0.1:3000/api (wildcard)
  web: http://127.0.0.1:3000 (wildcard)
  kv-explorer: http://127.0.0.1:3000/internal/kv-explorer (wildcard)
```

Once the application started, you can open the KV explorer and add your OpenAI API key using the `openai_key` key.

### Building and running

Prerequisites:

- [Spin](https://developer.fermyon.com/spin)
- [the Spin JavaScript toolchain](https://developer.fermyon.com/spin/javascript-components)
- [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- an [OpenAI API key](https://openai.com/blog/openai-api)

Once you have configured Spin and the JavaScript toolchain locally, install the
dependencies for the API component:

```
$ cd api && npm install
```

Now, you can build the application and run it locally with Spin:

```bash
$ spin build
$ spin up
Serving http://127.0.0.1:3000
Available Routes:
  api: http://127.0.0.1:3000/api (wildcard)
  web: http://127.0.0.1:3000 (wildcard)
  kv-explorer: http://127.0.0.1:3000/internal/kv-explorer (wildcard)
```

The OpenAI client is based on the [work done by Eric Lewis](https://github.com/ericlewis/openai-node),
modified to use the `fetch` API.
