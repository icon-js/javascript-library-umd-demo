# javascript-library-umd-demo
Creating a UMD JavaScript library



```bat
npm init -y

npm i -D webpack webpack-cli babel-loader @babel/core @babel/preset-env
```

Scaffold the library
```bat
## Linux
mkdir -p {src,dist,examples/browser,examples/node}

touch src/index.js examples/browser/index.html examples/node/example.js

## Windows
mkdir src dist examples\browser examples\node

type nul > src/index.js
type nul > examples/browser/index.html
type nul > examples/node/example.js
```

folder structure should look like this:
```bat
.
├── dist
├── examples
│   ├── browser
│   │   └── index.html
│   └── node
│       └── example.js
└── src
    └── index.js
```