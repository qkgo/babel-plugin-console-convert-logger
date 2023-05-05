# babel-plugin-console-convert-logger

A Babel plugin to convert console.log statements to a custom logger function for better logging control in your JavaScript applications.

## Features

- Replaces all `console.log` calls with a custom logger function.
- Helps you manage and control log messages in your application.
- Easy to configure and integrate into your project.

## Installation

Using npm:
```sh
npm install --save-dev babel-plugin-console-convert-logger
```

Using yarn:
```sh
yarn add -D babel-plugin-console-convert-logger
```

## Usage
1. Add the plugin to your Babel configuration file (.babelrc or babel.config.js):
```json
{
  "plugins": [
    "babel-plugin-console-convert-logger"
  ]
}
```

2. Configure the plugin with the desired logger function:
```json
{
  "plugins": [
    ["babel-plugin-console-convert-logger", {
      "loggerFunction": "yourCustomLoggerFunction"
    }]
  ]
}
```
Replace yourCustomLoggerFunction with the name of the function you want to use for logging.

3. Implement the custom logger function in your application:
```javascript
function yourCustomLoggerFunction(message, ...args) {
  // Your custom logging logic
}
```
Now, all instances of console.log in your application will be replaced with calls to yourCustomLoggerFunction.

License
MIT License. See LICENSE for more information.
