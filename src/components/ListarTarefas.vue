<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    tarefas: {
        type: Array,
        required: true
    },
    realizadas: {
        type: Boolean,
        default: false
    }
});
</script>

<template>
    <section v-for="tarefa in props.tarefas" :key="tarefa.id" :class="{ 'feita': tarefa.feita }"
        @click="$emit('click', tarefa.id)">
        <Transition name="fade">
            <p v-if="props.realizadas ? tarefa.feita : !tarefa.feita">{{ tarefa.descricao }}</p>
        </Transition>
    </section>
</template>

<style scoped>
.feita {
    text-decoration: line-through;
}

.fade-enter-active,
.fade-leave-active {
    transition: opacity 2s ease-in-out;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>
