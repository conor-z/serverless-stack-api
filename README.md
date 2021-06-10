# Notes api

```
Service Information
service: notes-api
stage: prod
region: us-east-1
stack: notes-api-prod
resources: 32
api keys:
  None
endpoints:
  POST - https://aibwsbei28.execute-api.us-east-1.amazonaws.com/prod/notes
  GET - https://aibwsbei28.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
  GET - https://aibwsbei28.execute-api.us-east-1.amazonaws.com/prod/notes
  PUT - https://aibwsbei28.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
  DELETE - https://aibwsbei28.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
functions:
  create: notes-api-prod-create
  get: notes-api-prod-get
  list: notes-api-prod-list
  update: notes-api-prod-update
  delete: notes-api-prod-delete
layers:
  None
```

### Installation

To create a new Serverless project.

``` bash
$ serverless install --url https://github.com/AnomalyInnovations/serverless-nodejs-starter --name my-project
```

Enter the new directory

``` bash
$ cd my-project
```

Install the Node.js packages

``` bash
$ npm install
```

### Usage

To run a function on your local

``` bash
$ serverless invoke local --function hello
```

To simulate API Gateway locally using [serverless-offline](https://github.com/dherault/serverless-offline)

``` bash
$ serverless offline start
```

Deploy your project

``` bash
$ serverless deploy
```

Deploy a single function

``` bash
$ serverless deploy function --function hello
```

#### Running Tests

Run your tests using

``` bash
$ npm test
```

We use Jest to run our tests. You can read more about setting up your tests [here](https://facebook.github.io/jest/docs/en/getting-started.html#content).

#### Environment Variables

To add environment variables to your project

1. Rename `env.example` to `.env`.
2. Add environment variables for your local stage to `.env`.
3. Uncomment `environment:` block in the `serverless.yml` and reference the environment variable as `${env:MY_ENV_VAR}`. Where `MY_ENV_VAR` is added to your `.env` file.
4. Make sure to not commit your `.env`.
