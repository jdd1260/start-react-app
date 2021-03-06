# Quickstart-React

Superpowered [Create React App](https://github.com/facebook/create-react-app).


## Quick Overview

[Create React App](https://github.com/facebook/create-react-app) is great, but it merely gets you started. Chances are you're still going to need to do some configuration and setup. Quickstart-React is here to help, adding these features on top of what Create React App gives you:

* [Redux](http://redux.js.org/) and [React-Redux](https://github.com/reactjs/react-redux) provides an enhanced state management framework and integration with React.
* [Sass](http://sass-lang.com) is the CSS extension language to supercharge your CSS development.
* [Bootstrap](http://getbootstrap.com/) for improved styling and mobile-first design.
* [redux-promise](https://github.com/acdlite/redux-promise) is Redux middleware to add support for nice handling of promises. This is great when using REST APIs.
* [prop-types](https://www.npmjs.com/package/prop-types) for defining and checking React prop types.
* [Storybook](https://storybook.js.org/) for UI component development.
* [Jest](https://facebook.github.io/jest/) with [Enzyme](https://github.com/airbnb/enzyme) all set up for easy React component testing.
* [ESLint](https://eslint.org/) with Facebook's [eslint-config-react-app](https://github.com/facebook/create-react-app/tree/master/packages/eslint-config-react-app) for style linting.

Additionally, you are provided with a new tool to speed up development, not just the creation, of your project. You can quickly generate new components with all boilerplate completed for you. A component is made up of:
* A Redux-connected component
* An actions file (optional)
* A reducer, connected to your global state (optional)
* Tests set up for each of those generated files

** Note: Quickstart-react is not a fork of [Create React App](https://github.com/facebook/create-react-app), but a fork of the `react-scripts` package with additional features added. To learn more about the functionality of Create React App, please read their [documentation](https://github.com/facebook/create-react-app).

### Get Started

1. Install [Yarn](https://yarnpkg.com/en/docs/install)
2. Run create-react-app: `yarn create react-app my-app --scripts-version quickstart-react-scripts`
3. Navigate to your new project and start a local server: `cd my-app && yarn start`

**You’ll need to have Node >= 8 on your local development machine** (but it’s not required on the server). You can use [nvm](https://github.com/creationix/nvm#installation) (macOS/Linux) or [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) to easily switch Node versions between different projects.


It will create a directory called `my-app` inside the current folder.<br>
Inside that directory, it will generate the initial project structure and install the transitive dependencies.

No configuration or complicated folder structures, just the files you need to build your app.<br>
Once the installation is done, you can open your project folder:

```sh
cd my-app
```

Inside the newly created project, you can run some built-in commands:

### `yarn new-component`

This tool is designed to speed the creation of new redux-connected components. It creates a new component in the `src/components` directory. You will be prompted for a component name. Then you have the option to create actions, a reducer, a .scss file, and a Storybook story for the component. If you were to give a component name of `Item` and agree to all options, your file structure will look like:

```
my-app/
  src/
    components/
      item/
        actions.js
        actions.test.js
        index.js
        index.scss
        index.test.js
        reducer.js
        reducer.test.js
        stories.js
```

Your component (in `index.js`) is tested and comes plugged into the generated actions, which are connected to the reducer. The reducer is connected to the global state through `src/reducers.js`. Each of these files is functioning and tested right from the start.

### `yarn start`

Runs the app in development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will automatically reload if you make changes to the code.<br>
You will see the build errors and lint warnings in the console.

### `yarn test`

Runs the test watcher in an interactive mode.<br>
By default, runs tests related to files changed since the last commit.
You may also run `yarn coverage` to see an analysis of your test coverage.


[Read more about testing.](https://github.com/jdd1260/quickstart-react/blob/master/packages/react-scripts/template/README.md#running-tests)

### `yarn lint`

This will run [ESLint](https://eslint.org/) on your JavaScript files. It runs the rules from Facebook's [eslint-config-react-app](https://github.com/facebook/create-react-app/tree/master/packages/eslint-config-react-app). You can change the rules used by modifying `.eslintrc.json`.

### `yarn build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
By default, it also [includes a service worker](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app) so that your app loads from local cache on future visits.

Your app is ready to be deployed.
