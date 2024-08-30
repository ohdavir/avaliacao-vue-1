<script setup>
import { ref, defineEmits } from 'vue';

const model = ref('');
const emit = defineEmits();

const adicionarTarefa = () => {
    if (model.value.trim() !== '') {
        emit('adicionarTarefa', model.value);
        model.value = '';
    }
};
</script>

<template>
    <section>
        <h2>Adicione uma nova tarefa</h2>
        <input type="text" v-model="model" @keyup.enter="adicionarTarefa" />
        <button @click="adicionarTarefa">Adicionar</button>
    </section>
</template>

<style scoped>
input {
    border-radius: 10px;
    border: solid 2px gray;
    padding: 5px;
    margin: 5px 0;
}


button {
    border-radius: 10px;
    border: solid 2px rgb(38, 99, 190);
    background-color: rgb(52, 124, 231);
    color: #ffffff;
    padding: 5px;
    margin: 5px 0 0 10px;

}

section {
    border-radius: 20px;
}
</style>