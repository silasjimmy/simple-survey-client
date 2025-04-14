# Simple Survey Client

## Tools

- [Vue](https://vuejs.org/)

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) to make the TypeScript language service aware of `.vue` types.

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

### API endpoint

Create a _.env.development_ file in the _application-src_ folder and add the following environment variable:

```
VITE_API_ENDPOINT=http://127.0.0.1:5000/api
```

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Run Unit Tests with [Vitest](https://vitest.dev/)

```sh
npm run test:unit
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

## Deployment

The web application is deployed using the [firebase hosting](https://firebase.google.com/docs/hosting) service.

The deployment process is streamlined and automated using Github Actions CI/CD tool. The process works as follows:

1. Developer makes a change in a separate branch and pushes the changes to the remote repo.
2. Developer raises a PR to the `development` or `main` branch.
3. Github Actions builds and deplys the web application to a preview channel where the developer can canfirm the changes made on a live development environment.
4. Once every change is confirmed and verified, the changes are merged to the `main` branch.
5. Github Actions builds and deploys the web application to the production environment.

- The deployed web application can be accessed using this link: [Sky World Survey](https://sky-world-survey.web.app/)
> The web application might take around 30 seconds to function optimally. The delay is due to the time taken by the API instance to spin up due to inactivity.