// SFC Single File Componet
<template>
    <form>
        <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label">Họ tên</label>
            <input v-model="user.name" type="text" class="form-control" id="" >
        </div>
        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">Tuổi</label>
            <input v-model="user.age" type="text" class="form-control" id="">
        </div>
    </form>


    <div class="">
        <h1>Thông tin đã nhập</h1>
        <p>Họ và tên: {{ user.name }}</p>
        <p>Tuổi: {{ user.age }}</p>

    </div>


</template>

<script setup>
import { reactive, ref } from 'vue';


const user = reactive({
    name: null,
    age: null
});




</script>

<style scoped></style>