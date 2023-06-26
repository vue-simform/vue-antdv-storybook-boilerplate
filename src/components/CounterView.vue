<script setup lang="ts">
    import { ref } from 'vue';
    const count = ref(0);
    function increment() {
        count.value++;
    }
    function decrement() {
        count.value--;
    }
    // return { number, increment, decrement };

</script>

<template>
    <h1 class="counter_heading">Counter : </h1>
    <div class="counter_buttons_section">
        <a-button type="primary" shape="round" size="large" @click="increment"><span class="counter_buttons">Increment</span></a-button>
        <h2 class="counter_result">{{ count }}</h2>
        <a-button type="primary" shape="round" size="large" @click="decrement"><span class="counter_buttons">Decrement</span></a-button>
    </div>
</template>

<style scoped>
.counter_heading {
    text-align: center;
    font-weight: bold;
}
.counter_buttons_section {
    text-align: center;
    margin-top: 2rem;
}
.counter_buttons {
    font-weight: bold;
}
.counter_result {
    margin: 1rem 0;
}
</style>
