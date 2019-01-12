# Build App

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

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


# <img src="https://cdn.vuetifyjs.com/images/logos/v-alt.svg" width="30" height="30"> Vuetify 
> Add vuetify plugin into nuxt guide:

### 1. Install External Packages
	npm install --save vuetify

### 2. Install stylus-loader
> In order to have ability use any stylus package version, it won't be installed automatically. So it's required to add it to package.json along with stylus-loader.
>
> The latest version supporting webpack 1 can be installed with:

	npm install stylus-loader stylus --save-dev

### 3. Create plugin called vuetify.js in plugins and add this code.

	import Vue from 'vue'
	import Vuetify from 'vuetify'

	Vue.use(Vuetify)

### 4. In nuxt.config.js add the following.

    head: {
        link: [
          { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Roboto:100,300,400,500,700,900|Material+Icons' },
        ]
    },
        
    plugins: ['~plugins/vuetify.js'],

    css: ['~assets/css/app.styl'],

    plugins: ['~plugins/vuetify.js'],

    css: [
        {
            src: join(__dirname, 'assets/css/app.styl'),
            lang: 'styl'
        }
    ],

    build: {
        vendor: ['vuetify'],
    }

### 5. In assets folder create css folder and file called app.styl add this content

	@require '~vuetify/src/stylus/settings/_colors'
    
    $theme := {
    primary:     $red.darken-2
    accent:      $red.accent-2
    secondary:   $grey.lighten-1
    info:        $blue.lighten-1
    warning:     $amber.darken-2
    error:       $red.accent-4
    success:     $green.lighten-2
    }
  
    // Import Vuetify styling
    @require '~vuetify/src/stylus/main'

