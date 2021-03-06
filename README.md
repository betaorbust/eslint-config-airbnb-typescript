# eslint-config-airbnb-typescript

> Airbnb's ESLint config with TypeScript support

Works with both JS and TS files.

## I use eslint-config-airbnb (with React support)

Install dependencies. ESLint plugins [must also be installed](https://github.com/eslint/rfcs/pull/5).

```bash
npm install eslint-config-airbnb-typescript \
            eslint-config-airbnb@^18.2.0 \
            eslint-plugin-import@^2.22.0 \
            eslint-plugin-jsx-a11y@^6.3.1 \
            eslint-plugin-react@^7.20.3 \
            eslint-plugin-react-hooks@^4.0.8 \
            @typescript-eslint/eslint-plugin@^3.6.1 \
            --save-dev
```

Within your ESLint config file:

```js
module.exports = {
  extends: ['airbnb-typescript'],
  parserOptions: {
    project: './tsconfig.json',
  },
};
```

Alter your `eslint` command to include `ts` and `tsx` files:

```bash
eslint --ext .js,.jsx,.ts,.tsx ./
```

## I use eslint-config-airbnb-base (no React support)

Install dependencies. ESLint plugins [must also be installed](https://github.com/eslint/rfcs/pull/5).

```bash
npm install eslint-config-airbnb-typescript \
            eslint-plugin-import@^2.22.0 \
            @typescript-eslint/eslint-plugin@^3.6.1 \
            --save-dev
```

Within your ESLint config file:

```js
module.exports = {
  extends: ['airbnb-typescript/base'],
  parserOptions: {
    project: './tsconfig.json',
  },
};
```

Alter your `eslint` command to include `ts` and `tsx` files:

```bash
eslint --ext .js,.jsx,.ts,.tsx ./
```

## I wish this config would support [...]

The goal of `eslint-config-airbnb-typescript` is decorate `eslint-config-airbnb` with TypeScript support. All rules and settings are identical. It's a drop-in replacement for `eslint-config-airbnb`, including linting for JavaScript files.

It's recommended to alter your ESLint config for additional functionality. Here's an example:

```js
{
  "extends": [
    "airbnb-typescript",
    "airbnb/hooks",
    "plugin:@typescript-eslint/recommended",
    "plugin:@typescript-eslint/recommended-requiring-type-checking"
  ],
}
```

My personal ESLint config file with support for Jest, Promises, and Prettier can be found in [create-exposed-app](https://github.com/iamturns/create-exposed-app/blob/master/.eslintrc.js).

## Additional Documentation

- [CHANGELOG.md](CHANGELOG.md)
- [DEVELOPING.md](DEVELOPING.md)
- [CONTRIBUTING.md](CONTRIBUTING.md)
- [MAINTAINING.md](MAINTAINING.md)

## Credits

Authored and maintained by Matt Turnbull ([iamturns.com](https://iamturns.com) / [@iamturns](https://twitter.com/iamturns))

To all [contributors](https://github.com/iamturns/eslint-config-airbnb-typescript/graphs/contributors) (if you exist) - thank you!

## License

Open source [licensed as MIT](https://github.com/iamturns/eslint-config-airbnb-typescript/blob/master/LICENSE).
