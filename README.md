# react-extension
chrome react-extension ui

Installation

# Make sure both is installed globally
npm install -g yo
npm install -g generator-react-webpack
Setting up projects

# Create a new directory, and `cd` into it:
mkdir my-new-project && cd my-new-project

# Run the generator
yo react-webpack
Please make sure to edit your newly generated package.json file to set description, author information and the like.

Generating new components

# After setup of course :)
# cd my-new-project
yo react-webpack:component my/namespaced/components/name

Generating new stateless functional components

yo react-webpack:component my/namespaced/components/name --stateless

Usage

The following commands are available in your project:

# Start for development
npm start # or
npm run serve

# Start the dev-server with the dist version
npm run serve:dist

# Just build the dist version and copy static files
npm run dist

# Run unit tests
npm test

# Auto-run unit tests on file changes
npm run test:watch

# Lint all files in src (also automatically done AFTER tests are run)
npm run lint

# Clean up the dist directory
npm run clean

# Just copy the static assets
npm run copy
Naming Components

We have opted to follow @floydophone convention of uppercase for component file naming e.g. Component.js. I am open to suggestions if there is a general objection to this decision.

Modules
https://github.com/react-webpack-generators/generator-react-webpack-alt#generating-new-components
Each component is a module and can be required using the Webpack module system. Webpack uses Loaders which means you can also require CSS and a host of other file types. Read the Webpack documentation to find out more.


Installation

npm install -g yo
npm install -g generator-react-webpack-alt
Setting up projects

# Create a new directory, and `cd` into it:
mkdir my-new-project && cd my-new-project

# Run the generator
yo react-webpack-alt
Generating new components

yo react-webpack-alt:component my/namespaced/components/name
Generating new stores and actions

# After setup of course :)
# cd my-new-project
yo react-webpack-alt:action my/namespaced/actions/name
yo react-webpack-alt:store my/namespaced/stores/name

# Create a new store, as well as a dedicated action for it
yo react-webpack-alt:all my/namespaced/functions/name
Generating sources

Stores in alt.js can use so called sources to make the usage of async actions easier for you. Please look at the alt.js documentation for this feature to see how this can be implemented.

You can create an empty source by using the following command:

yo react-webpack-alt:source my/namespaced/sources/name
You will then be able to include it in your stores via

import NameSource from 'sources/my/namespaces/sources/nameSource';
NameSource.remoteAction();
Usage

Please take a look at react-webpack-template for an in depth explanation or use npm run to get a list of all commands available for building and running your application.

Basics are:

npm start: Will start up the dev webserver
npm test: Run unit tests
npm run dist: Create the packed version
Contribute

Contributions are welcomed. If you find something is missing or there are errors hidden somewhere, feel free to add a new issue.

Running Tests

npm test or node node_modules/.bin/mocha


Installation

npm install -g yo
npm install -g generator-react-webpack-redux
Global npm packages

Install the following packages system wide, to decrease the time needed to scaffold a new project:

npm install -g phantomjs-prebuilt
Setting up projects

# Create a new directory, and `cd` into it:
mkdir my-new-project && cd my-new-project

# Run the generator
yo react-webpack-redux
Generating new reducers

yo react-webpack-redux:reducer my/namespaced/reducers/name
yo react-webpack-redux:reducer items
Generating new actions

yo react-webpack-redux:action my/namespaced/actions/name
yo react-webpack-redux:action addItem
Generating new components

yo react-webpack-redux:component my/namespaced/components/name
yo react-webpack-redux:component button
Generating new containers

yo react-webpack-redux:container my/namespaced/container/Name
yo react-webpack-redux:container wrapper
Usage

Please take a look at react-webpack-template for an in depth explanation or use npm run to get a list of all commands available for building and running your application.

Basics are:

npm start: Will start up the dev webserver
npm test: Run unit tests
npm run dist: Create the packed version
