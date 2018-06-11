<template>
    <button v-bind:class="classes" 
            @click="Increase()">
        Számláló: {{ counterPlusOffset }}
    </button>
</template>

<script>
export default {
    props: ['theme', 'offset'],
    data: function() {
        return {
            counter: 1
        };
    },
    computed: {
        counterPlusOffset() {
            return +this.offset + this.counter;
        },
        classes() {
            return ['btn', 'btn-' + this.theme];
        }
    },
    methods: {
        Increase() {
            this.counter++;
        }
    }
};
</script>
 
<style lang="scss" scoped>
button {
    &.btn {
        margin: 0 1rem;
    }
}
</style> 
