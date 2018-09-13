# deploy-app
Lightweight deployment option for apps, projects and stuff

```sh
$ deploy-app deploy prod
```

[![NPM version](https://img.shields.io/badge/deploy--app-v1.0.0-blue.svg)](https://www.npmjs.com/package/env-path)
## Installation

```sh
$ npm install deploy-app
```

## Usage

### Init
Run in your project

```sh
$ deploy-app init
```

Adds a `deploy-app.json` config file to your projects
production


```json
{
  "prod":{
    "user": "deploy",
    "host": "192.168.0.1",
    "port": "22",
    "files": "build src *.json app.js",
    "path": "~/myProject",
    "pre-deploy" : "[ -d myProject ] || mkdir myProject ",
    "post-deploy" : "npm install --production; node app.js"
  },
  "dev":{},
  "staging":{}
}
```


### Deploy
Chose a environment to deploy: `prod`

```sh
$ deploy-app deploy prod
```

That's it.<br>
Happy coding!

## License

  [MIT](LICENSE)
