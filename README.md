# vuejs-vue-jest-ts-unexpected-token-repro

Made from `vue create vuejs-vue-jest-ts-unexpected-token-repro` with:

```
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, TS, Linter, Unit
? Use class-style component syntax? No
? Use Babel alongside TypeScript for auto-detected polyfills? Yes
? Pick a linter / formatter config: TSLint
? Pick additional lint features: (Press <space> to select, <a> to toggle all, <i> to invert selection)Lint on save
? Pick a unit testing solution: Jest
? Where do you prefer placing config for Babel, PostCSS, ESLint, etc.? In dedicated config files
? Save this as a preset for future projects? No
```

**Running the `npm run test:unit` fails:**

```
> vue-cli-service test:unit

 FAIL  tests/unit/example.spec.ts
  ● Test suite failed to run

    /Users/francois/vuejs-vue-jest-ts-unexpected-token-repro/node_modules/bootstrap-vue/es/components/table/table.js:3
    import startCase from 'lodash.startcase';
           ^^^^^^^^^

    SyntaxError: Unexpected identifier

       7 |
       8 | <script lang="ts">
    >  9 | import bTable from 'bootstrap-vue/es/components/table/table';
         | ^
      10 | import Vue from 'vue';
      11 |
      12 | const demoItems = [

      at ScriptTransformer._transformAndBuildScript (node_modules/jest-runtime/build/script_transformer.js:403:17)
      at src/components/HelloWorld.vue:9:1
      at Object.<anonymous> (src/components/HelloWorld.vue:56:3)

Test Suites: 1 failed, 1 total
Tests:       0 total
Snapshots:   0 total
Time:        5.723s
Ran all test suites.
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! vuejs-vue-jest-ts-unexpected-token-repro@0.1.0 test:unit: `vue-cli-service test:unit`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the vuejs-vue-jest-ts-unexpected-token-repro@0.1.0 test:unit script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/francois/.npm/_logs/2019-02-08T08_13_10_343Z-debug.log
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Run your unit tests
```
npm run test:unit
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
