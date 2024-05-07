<script setup>
import { ref } from 'vue';

const text = ref('');
const textColor = ref('black');
const backgroundColor = ref('#f4f4f4');

function toggleTextColor() {
    textColor.value = textColor.value === 'black' ? 'red' : 'black';
}

function toggleBackgroundColor() {
    backgroundColor.value = backgroundColor.value === '#f4f4f4' ? '#e6e6e6' : '#f4f4f4';
}
</script>

<template>
    <input v-model="text" placeholder="Ketik disini"><br>
    <p :style="{ color: textColor, backgroundColor: backgroundColor }">{{ text }}</p>

    <button @click="toggleTextColor">Ubah Warna Teks</button>
    <button @click="toggleBackgroundColor">Ubah Warna Latar Belakang</button>
</template>



<style>
    body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
        padding: 20px;
    }

    input {
        padding: 10px;
        margin-bottom: 10px;
        font-size: 16px;
        border-radius: 5px;
        border: 1px solid #ccc;
    }

    p {
        font-size: 18px;
        padding: 10px;
        border-radius: 5px;
        background-color: #fff;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        transition: color 0.3s ease-in-out;
    }

    button {
        padding: 10px 20px;
        font-size: 16px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s ease-in-out;
    }

    button:hover {
        background-color: #0056b3;
    }
</style>