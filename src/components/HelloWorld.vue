<template lang="pt-br">
  <div>
      <button @clcik="comentar">
          Comentar
      </button>
      <p>
          {{ comentario }}
      </p>
      <p>
          Nome: {{ nome }}
      </p>
  </div>
</template>

<script lang="ts">

import Vue from 'vue'
import Component from 'vue-class-component'

import { Prop } from 'vue-property-decorator'

@Component
export default class Comentarista extends Vue {

  private comentario = ''
  @Prop() private nome: string

  private comentar() : void {
      this.comentario = 'Um mega comentário bem complexo!'
  }

}
</script>
