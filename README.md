# javascript-library-umd-demo
Creating a UMD JavaScript library



```bat
npm init -y

npm i -D webpack webpack-cli babel-loader @babel/core @babel/preset-env
```

Scaffold the library
```bat
mkdir -p {src,dist,examples/browser,examples/node}

touch src/index.js examples/browser/index.html examples/node/example.js
```