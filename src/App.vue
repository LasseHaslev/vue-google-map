<template>
    <div id="app">
        <div class="hero is-info">
            <div class="hero-body">
                <div class="container">
                    <h1 class="title">&#60;vue-google-map></h1>
                    <h3 class="subtitle">&#60;google-map :lat="59.9139" :lng="10.7522"></google-map&#62;</h3>
                </div>
            </div>
        </div>
        <section class="section">
            <div class="container">
<pre>&#60;template>
    &#60;div style="height 300px">
        &#60;google-map @ready="mapReady" :lat="59.9139" :lng="10.7522">&#60;/google-map>
    &#60;/div>
&#60;/template>
&#60;script>
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
&#60;/script>
</pre>
            </div>
        </section>
        <div id="map">
            <google-map :lat="59.9139" :lng="10.7522"></google-map>
        </div>
    </div>
</template>

<script>
import GoogleMap from './index.js';
export default {

    name: 'app',

    components: {

        GoogleMap,

    }

}
</script>

<style>
html, body, #app {
    height: 100%;
}

#app {
    display: flex;
    flex-direction: column;
}

#map {
    min-height: 400px;
    flex: 1;
    background-color: red;
}
</style>
