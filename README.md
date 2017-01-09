# @lassehaslev/vue-google-map

> Google map for use with vue

## Install

Run ```npm install @lassehaslev/vue-google-map --save``` in your project folder.

## Usage

```js
<template>
    <div style="height 300px">
        <google-map @ready="mapReady" :lat="59.9139" :lng="10.7522"></google-map>
    </div>
</template>
<script>
import GoogleMap from '@lassehaslev/vue-google-map';
export default {
    name: 'app',

    methods: {
        mapReady( map, google ) {
            new google.maps.Map(...);
        }
    },

    components: {
        GoogleMap,
    }
}
</script>
```


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
