# javascript-library-umd-demo
Creating a UMD JavaScript library


### Initialize NPM package and install Node.js dependencies
```bat
npm init -y

npm i -D webpack webpack-cli babel-loader @babel/core @babel/preset-env
```

### Scaffold the library
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

### Bundle the library
```bat
## Linux
touch webpack.config.js .babelrc

## Windows
type nul > webpack.config.js
type nul > .babelrc
```

webpack.config.js
```javascript
const path = require('path');module.exports = {
	mode: 'production',
	entry: './src/index.js',
	output: {
		path: path.resolve(__dirname, './dist'),
		filename: 'calculator.js',
		library: 'calculator',
		libraryTarget: 'umd',
		globalObject: 'this',
	},
	module: {
		rules: [{
			test: /\.js$/,
			exclude: /(node_modules)/,
			use: 'babel-loader',
		}],
	},
};
```

.babelrc
```json
{
	"presets": ["@babel/preset-env"]
}
```