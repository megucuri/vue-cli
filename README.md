# real-world-vue

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).



## From Scratch ##

### Creating project and enviorment with CLI
```
$ vue create project_name
$ cd project_name
$ yarn run serve/npm run serve
```

### Creating project with UI
```
$ vue ui
```
### Basic Project Structure

- Nod_modules: The libraries/dependencies to build project<br>
- Public: File not wanting to be processed by Webpack. e.g. images.<br>
- Src: All the application code goes. <br>
- Assets: images, fonts, css, etc<br>
- Components: Store building blocks of Vue app<br>
- Views: Store different ‘pages’<br>
- App.js : root component that all other components are nested in.<br>
- Main.js: renders app and mounts it to the DOM<br>
- Router.js<br>
- Store.js: for Vuex<br>
- babel.config.js<br>
- Package.js: help yarn/npm identify projects and handles its dependencies

### How pages are loaded

1. App,js has all the components nested <br>
2. main.js takes app.js and renders it then mounts it to HTML file where the id=“app” lives.<br>
3. Our app appears on the DOM

### Build Process

Webpack will be bundling all our files together
```
$ yarn run build // This will make a dist folder
```
#### In index.html in the dist folder two script tags has been added
```
<script src=/js/chunk-vendors.c6093fef.js></script> //points to all are dependencies<br>
<script src=/js/app.4e9b2e36.js></script> // App specific code including the code in main.js which renders and mounts the app
```
### Adding Plugins
```
$ vue add vuetify
```
from:<br>
https://www.vuemastery.com/courses/real-world-vue-js/vue-cli


## From tutorial
Download Vetur, ESLint, Prettier plugin.<br>
Then do the following.
```
// .eslintrc.js

...
 extends: [
    'plugin:vue/essential',

    // After installing the ES Lint and Prettier extention configure Prettier for this project.
    '@vue/prettier',
    'plugin:prettier/recommended'
  ],
...


// Create .prettierrc.js

/*
 We make this file for Prettify

 Set this up as anyway you prefer

 */

module.exports = {
  singleQuote: true, // This will convert double quotes to single quotes,
  semi: false // Make sure that semicolons are not automatically inserted.
}

```

