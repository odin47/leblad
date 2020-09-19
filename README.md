# Le'Blad

A library providing a list of Algerian administrative areas with many useful APIs.

## Getting started

### Usage

#### Node.js

```javascript
const lebledSdk = require('leblad');

// Example: get a full list of Algerian provinces (Wilayas)
console.log(leblad.getWilayaList());
```

#### API

##### getWilayaList(projection?: string[])

Returns a list of Algerian provinces (Wilayas)

**Arguments**

`projection: string[]` (optional) Array of Wilaya Object attributes.

**Examples**

```javascript
const { getWilayaList } = require('leblad');

const allWilayasDetails = getWilayaList();

// if we only want the wilaya names for example:
const wilayasNames = getWilayaList(['name', 'name_ar', 'name_en']);

```

### Local development

#### Perquisites

Make sure you have:

- [Git](https://git-scm.com/)
- [Nodejs](https://nodejs.org/) version 10 or higher

#### Install the dependencies

```
npm install
```

#### Update the Wilayas dataset

```
npm run update-dataset
```

#### Testing

Simply run

```
npm test
```

Or this command for the `watch mode`:

```
npm run test.watch
```

You can also run [mutation tests](https://en.wikipedia.org/wiki/Mutation_testing) (using [Stryker-mutator](https://stryker-mutator.io/))

```
npm run test.mutation
```

## Contributing

When contributing to this repository, please first discuss the change you wish to make by opening an [issue](https://github.com/dzcode-io/leblad/issues/new/choose), sending an e-mail, or any other method with us before making a change.

And also, please make sure to read our [guidelines for contributing](./.github/CONTRIBUTING.md).

## Similar projects

- [dz-communes](https://github.com/AM-77/dz-communes) An NPM package exposing a list of all of the 48 wilayas of Algeria and their communes.
- [algeria-api](https://github.com/fcmam5/algeria-api) An web API exposing Wilayas data. We data from that project as a source of truth for ([data/WilayaList.json](./data/WilayaList.json))

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details
