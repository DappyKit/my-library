# MyLibrary: A TypeScript + Jest + Webpack Template for Node.js and Browser Libraries

Welcome to MyLibrary, a ready-to-use TypeScript template for building libraries that can run in both Node.js and the browser. This project is bundled with Jest for testing and Webpack for building your library.

## Table of Contents
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)
- [GitHub Actions](#github-actions)
- [Customizing the Library](#customizing-the-library)

## Getting Started
To get started, clone this repository to your local machine and run `npm ci`.

`npx @dappykit/my-library my-new-lib`

## Project Structure
Here's a brief overview of the key files and directories in this template:

- `src/`: The source code of your library. The entry point of the library is `src/index.ts`.
- `test/`: Contains the tests for your library.
- `.github/workflows/`: Contains configuration for GitHub Actions workflows.
- `.babelrc.js`: Configures Babel, a JavaScript compiler.
- `.eslintrc.json`: Configures ESLint, a tool for identifying and reporting on patterns in JavaScript.
- `jest.config.js`: Configures Jest, a JavaScript testing framework.
- `tsconfig.json`: Configures TypeScript for the project.
- `webpack.config.ts`: Configures Webpack for bundling the library.

## Available Scripts
This template includes the following scripts:

- `npm run prepublishOnly`: Cleans the `dist` directory and compiles TypeScript files to JavaScript. It also prepares the library for both Node.js and browser environments.
- `npm run test`: Runs the Jest test suite.
- `npm run lint:check`: Lints the codebase using ESLint and checks for formatting issues with Prettier.
- `npm run check:types`: Checks for TypeScript type errors.
- `npm run compile:node`: Compiles the code for Node.js using Webpack.
- `npm run compile:types`: Compiles the TypeScript declarations.
- `npm run compile:browser`: Compiles the code for the browser using Webpack.

## GitHub Actions
This template includes three GitHub Actions workflows:

- `tests.yaml`: Runs tests, checks for type errors, and lints the code whenever changes are pushed or a pull request is created.
- `publish_npmjs.yaml`: Publishes the package to npm when a new release is created on GitHub. You'll need to add your npm token to your repository's secrets under the name `NPM_TOKEN`.
- `release_github.yaml`: Creates a new release on GitHub whenever changes are pushed to the `master` branch. For this to work, you'll need to add a personal access token to your repository's secrets under the name `REPO_GHA_PAT`.

## Customizing the Library
To make this library your own, you'll need to change the following:

- Update `name`, `version`, `description`, and `author` in `package.json`.
- If you want your library to be available under a different name in the `window` object when used in a browser, update the `library` key in the `output` object in `webpack.config.ts`. For example, if you want your library to be available as `MyNewLib`, you would set `library: 'MyNewLib'`.
- Write your library's code in the `src/` directory. You can organize your code in this directory any way you want. Don't forget to update `src/index.ts` if you add or remove files.
- Write tests for your library's code in the `test/` directory. Jest is configured to read all files in this directory that match the pattern `*.test.ts`.

This template should give you a strong starting point for building a library that can run in both Node.js and the browser. Happy coding!

---

Try [YumCut](https://yumcut.com)! This is an AI video generator that turns a single prompt into a ready-to-post vertical short video in minutes. It creates the script, images, voice-over, subtitles, and edits everything into a final clip automatically. It’s built for fast testing and making lots of variations without spending hours in an editor.
