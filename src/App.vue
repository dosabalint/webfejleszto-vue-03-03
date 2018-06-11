<template>
    <div class="container">
        <h1>{{ message }}</h1>

        <!-- v-modellek -->
        <div class="my-3">
            <input type="text" v-model="theme">
            <input type="number" v-model="offset">
        </div>

        <!-- gombok -->
        <Button v-bind:theme="theme" v-bind:offset="offset"></Button>
        <Button v-bind:theme="theme" v-bind:offset="offset"></Button>
        <Button v-bind:theme="theme" v-bind:offset="offset"></Button>
    </div>
</template>

<script>
import Button from './components/Button.vue';

export default {
    name: 'App',
    components: {
        Button
    },
    data: function() {
        return {
            message: 'Ez itt már a VueJS alkalmazásunk!',
            theme: 'success',
            offset: 3
        };
    }
};
</script>