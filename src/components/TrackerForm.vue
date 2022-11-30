<template>
  <div class="box">
    <div class="columns">
      <div class="column is-8" role="form" aria-label="Formulário para criação de uma nova tarefa">
        <input 
          type="text"
          class="input"
          placeholder="Qual tarefa você deseja iniciar?"
          v-model="descricao"
        />
      </div>
      <div class="column">
        <TrackerTimerController @whenFinished="finalizarTarefa"/>
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
  data () {
    return {
      descricao: ''
    }
  },
  methods: {
    finalizarTarefa (tempoEmSegundos: number): void {
      console.log('tempo da tarefa: ', tempoEmSegundos)
      console.log('descricao: ', this.descricao)
      this.descricao = ''
    }
  }
})
</script>

<style scoped>

</style>