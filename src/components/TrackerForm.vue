<template>
  <div class="box">
    <div class="columns">
      <div class="column is-8" role="form" aria-label="Formulário para criação de uma nova tarefa">
        <input type="text" class="input" placeholder="Qual tarefa você deseja iniciar?" />
      </div>
      <div class="column">
        <TrackerTimerController/>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import TrackerTimerController from './TrackerTimerController.vue'
export default defineComponent({
  name: 'TrackerForm',
  components: {
    TrackerTimerController
  },
})
</script>

<style scoped>

</style>