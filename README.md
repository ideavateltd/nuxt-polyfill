**Warning:** This package is under development, will be published shortly

# nuxt-polyfill
Ease adding polyfills to your Nuxt.js project using [polyfill.io](polyfill.io) among others.

## Features
 - Easy to configure
 - Load polyfills **only if needed**
 - Aims to be as fast as possible
 - Supports polyfills from [polyfill.io](polyfill.io)
 - Supports custom polyfills

## Getting started
```
npm install nuxt-polyfill
```

Add the module to your `nuxt.config.js`: 

```javascript
export default {
    
    // Configure polyfills:
    polyfill: {
        features: [
            // Add features:
            {
                // Feature name of polyfill.io:
                feature: 'IntersectionObserver' 
                
                type: 'service',
                
                // Will be called client side on load
                detect: () => IntersectionObserver in window,
            },
            
            {
                // NPM package:
                feature: 'IntersectionObserver'
                
                type: 'custom',
                
                detect: () => IntersectionObserver in window,
                
                // Optional install function called client side after the package is required:
                install: () => { ... }
            }
        ]
    }
    
    // Add it to the modules section:
    modules: [
        'nuxt-polyfill',
    ]
}
```

## Examples
### Simple features

### Custom features

### Full Nuxt.js example projects
