// SFC Single File Componet
<template>
    <br>
    <button @click="handleCount" class="btn-success btn">click me</button>
    <h1 class="text-danger">Home nè</h1>
    <h2>InputText: {{ inputText }}</h2>
    <h2>Count: {{ count }}</h2>
    <hr>
    <input type="text" v-model="inputText" class="form-control">
    <hr>
    <div>
        <h3>User:</h3>
        <h4>Name: {{ user.name }} - Age: {{ user.age }}</h4>
    </div>
    <hr>
    <div>
        <ul v-for="user in users">
            <li>{{ user.name }}</li>
            <li>{{ user.age }}</li>
        </ul>
    </div>
    

</template>

<script setup>
import { reactive, ref } from 'vue';


const count = ref(0);
const inputText = ref('in bút tét');
const user = reactive({
    name: 'Hải Nam',
    age: 25
});

const users = reactive([
    { name: 'Hải Nam', age: 25 },
    { name: 'Hải Nam 1', age: 26 },
    { name: 'Hải Nam 2', age: 27 },
    { name: 'Hải Nam 3', age: 28 }
]);


// tăng biến số
const handleCount = () => {
    count.value++;
}



</script>

<style scoped></style>