# Webpack Angular

An example of using webpack with an Angular project.

See: https://egghead.io/lessons/angularjs-angular-with-webpack-introduction

#### Note: There are slight differences here due to running on Windows

## When creating a new app

### Install webpack 

#### Tips: 
- Add "engine.io-client": "automattic/engine.io-client" to package.json if you get socket.io compile errors on “npm install”

```
> npm install webpack webpack-dev-server -D
```

### Create webpack.config.js file in project root

```
module.exports = {
    entry: "./app/index.js",
    output: {
        path: __dirname + "/app",
        filename: "bundle.js"
    }
}
```

### Create bundle

```
> webpack
```

### Load bundle in index.html

```
<script src="bundle.js"></script>
```

## Live coding

### Delete bundle.js

### Add "start" script to package.json

#### Tip

- note that we are not using "webpack-dev-server" and NOT "node node_modules/.bin/webpack-dev-server"

```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack-dev-server --content-base app --progress --colors --port 8090",
    "build": "NODE_ENV=production node node_modules/.bin/webpack && cp app/index.html dist/index.html"
  },
```

### Start app

```
> npm start
```

#### Notes

- bundle.js is not created
- webpack serves bundle.js from memory

### Install Angular

```
> npm install angular
```
