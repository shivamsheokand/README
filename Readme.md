# nativewind for expo

`````bash
npx create-expo-app my-app

cd my-app
yarn add nativewind
yarn add --dev tailwindcss
npx tailwindcss init
```code
// tailwind.config.js

module.exports = {
content: ["./App.{js,jsx,ts,tsx}", "./<custom directory>/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```code
// babel.config.js
module.exports = function (api) {
  api.cache(true);
  return {
    presets: ["babel-preset-expo"],
   plugins: ["nativewind/babel"],
  };
};

```

```

```

# npm install tailwindcss@3.3.2 --save-dev

```bash
yarn remove nativewind
yarn remove tailwindcss
yarn add postcss@8.4.23
yarn add --dev tailwindcss@3.3.2
yarn add nativewind

yarn add nativewind
yarn add --dev tailwindcss@3.3.2
```

```bash
npm i -D postcss-loader@4.2.0 @expo/webpack-config
```

<!-- # npm i -D postcss-loader@4.2.0 @expo/webpack-config -->

````bash
webpack.config.
```code
// webpack.config.js
const createExpoWebpackConfigAsync = require("@expo/webpack-config");

module.exports = async function (env, argv) {
  const config = await createExpoWebpackConfigAsync(
    {
      ...env,
      babel: {
        dangerouslyAddModulePathsToTranspile: ["nativewind"],
      },
    },
    argv,
  );

  config.module.rules.push({
    test: /\.css$/i,
    use: ["postcss-loader"],
  });

  return config;
};
`````

```

```
