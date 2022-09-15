# shower-state
Website for viewing residence hall shower occupancy at UC Berkeley.

# Contributing
## Setup
### Database
Database hosted on [MongoDB](https://www.mongodb.com/). Mongo URI must be inlucded in a `.env` file:

```
MONGO_URI=<mongo_uri>
```

Because the URI includes a password, `.env` files will not be the repo. The `.env` file is stored in the root directory.

## Developing
### To develop locally:
1. Install dependencies for backend in the root directory:

    ```sh
    # in ./
    npm i
    ```

2. Install dependencies for frontend in the `/client` directory:

    ```sh
    # in ./
    cd client
    # now in ./client
    npm i
    ```

3. Run the backend. The main backend file is `/app/server.js`. During development, nodemon can be used to automatically restart the server when changes are made:

    ```sh
    # in ./
    npm run dev
    ```

4. The frontend can be run from the root directory:

    ```sh
    # in ./
    npm run client
    ```

### Linting
Linting is done with [ESLint](https://eslint.org/) and its config file is [here](./.eslintrc.json).
Please lint the codebase before commiting to the repo.

To lint codebase:

```sh
npm run lint
```

To use ESLint's autofix:

```sh
npm run lint-fix
```

Linting can also be done through the [VSCode ESLint Plugin](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint). ESLint is enabled as a formatter in the workspace settings store in `.vscode/settings.json`. To use the formatter, press `Shift + Alt + F` or `Cmd + Shift + P` and type `Format Document`.
